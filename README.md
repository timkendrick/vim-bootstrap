# vim-quickstart

> Sensible defaults for Vim newcomers

![Screenshot](screenshot.png)

## Background

This setup is aimed towards recent Vim converts. It provides an opinionated Vim configuration that comes loaded with all the key features that are typically bundled with a modern editor, while exposing the underlying power of Vim.

In other words, you'll still have to learn Vim, but at least you'll have all the tools you'd expect from a fully-fledged code editor.


## Installation

These instructions should be everything you need to get up and running, starting from a clean OS install.

### Mac OS X

1. Link the configuration files:

	```bash
	git clone https://github.com/timkendrick/vim-quickstart.git ~/vim-quickstart
	ln -s ~/vim-quickstart/.vimrc ~/.vimrc
	ln -s ~/vim-quickstart/.gvimrc ~/.gvimrc
	```

2. Install the [Vundle](https://github.com/VundleVim/Vundle.vim) package manager (used to install Vim plugins):

	```bash
	git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
	```

3. Install Vundle plugins:

	```bash
	vim -c PluginInstall -c bdelete -c quit
	```

4. Install [The Silver Searcher](https://github.com/ggreer/the_silver_searcher) (used by the [ag.vim](https://github.com/rking/ag.vim) plugin):

	```bash
	brew install the_silver_searcher
	```

5. Install the [Powerline fonts](https://github.com/powerline/fonts/archive/master.zip)

5. Install MacVim (optional, but recommended):

	```bash
	brew install macvim
	```

#### Mac OS X Installation notes

When launching Vim via Terminal.app, make sure **Terminal > Preferences > Profiles > Keyboard > Use Option as Meta key** is selected to enable all keyboard shortcuts.


## Terminal mode vs GUI mode

With this setup, Vim will run in one of two different modes depending on the launch environment:

- When launched in a terminal shell, Vim will run in **Terminal mode**. This loads a minimal set of plugins, which can be useful for fast editing of individual files.
- When launched in a GUI (e.g. MacVim or GVim), Vim will run in **GUI mode**. This loads a richer set of plugins for a more IDE-like experience, which can be useful when working within larger projects.


## Included plugins

| Plugin | Terminal mode | GUI mode | Purpose |
| ------ | :-----------: | :------: | ------- |
| [vim-surround](https://github.com/tpope/vim-surround) | ✔︎ | ✔︎ | Wrap code blocks |
| [vim-commentary](https://github.com/tpope/vim-commentary) | ✔︎ | ✔︎ | Code commenting |
| [vim-abolish](https://github.com/tpope/vim-abolish) | ✔︎ | ✔︎ | Smart word substitution |
| [vim-repeat](https://github.com/tpope/vim-repeat) | ✔︎ | ✔︎ | Repeat complex actions |
| [vim-move](https://github.com/matze/vim-move) | ✔︎ | ✔︎ | Shift lines up/down |
| [vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors) | ✔︎ | ✔︎ | Sublime-style multiple cursors |
| [emmet-vim](https://github.com/mattn/emmet-vim) | ✔︎ | ✔︎ | Dynamic HTML snippets |
| [NERDTree](https://github.com/scrooloose/nerdtree) | | ✔︎ | File explorer sidebar |
| [nerdtree-git-plugin](https://github.com/Xuyuanp/nerdtree-git-plugin) | | ✔︎ | Git status in file explorer |
| [vim-gitgutter](https://github.com/airblade/vim-gitgutter) | | ✔︎ | Git status in gutter |
| [vim-airline](https://github.com/bling/vim-airline) | | ✔︎ | Improved status bar |
| [YouCompleteMe](https://github.com/Valloric/YouCompleteMe) | | ✔︎ | Code completion |
| [Syntastic](https://github.com/scrooloose/syntastic) | | ✔︎ | Syntax checking
| [ag.vim](https://github.com/rking/ag.vim) | | ✔︎ | Fast code search |
| [vim-fugitive](https://github.com/tpope/vim-fugitive) | | ✔︎ | Git repository actions |
| [vim-bufonly](https://github.com/schickling/vim-bufonly) | | ✔︎ | Allow closing all inactive buffers |
| [editorconfig-vim](https://github.com/editorconfig/editorconfig-vim) | | ✔︎ | [Editorconfig](http://editorconfig.org/) support |
| [vim-colors-solarized](https://github.com/altercation/vim-colors-solarized) | | ✔︎ | [Solarized](http://ethanschoonover.com/solarized) color scheme |


## Included macros

| Macro | Terminal mode | GUI mode | Purpose |
| ----- | :-----------: | :------: | ------- |
| Matchit | ✔︎ | ✔︎ | Jump to block start/end |



## Keyboard mappings

| Keyboard shortcut | Action | Terminal mode | GUI mode |
| ----------------- | ------ | :-----------: | :------: |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>d</kbd> | Duplicate line | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>o</kbd> | Insert new line below cursor | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>o</kbd> | Insert new line above cursor | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>j</kbd> | Move line down | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>k</kbd> | Move line up | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>{</kbd> | Switch to previous buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>}</kbd> | Switch to next buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>w</kbd> | Close current buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>w</kbd> | Close all buffers except current buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Tab</kbd> | Toggle NERDTree sidebar | | ✔︎ |

See plugin documentation for additional keyboard mappings.
