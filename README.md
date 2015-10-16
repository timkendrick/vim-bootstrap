# vim-quickstart

> Sensible defaults for Vim newcomers

![Screenshot](screenshot.png)

## Background

This setup is aimed towards recent Vim converts. It provides an opinionated Vim configuration that comes loaded with all the key features that are typically bundled with a modern editor, while exposing the underlying power of Vim.

In other words, you'll still have to learn Vim, but at least you'll have all the tools you'd expect from a fully-fledged code editor.


## Installation

These instructions should be everything you need to get up and running, starting from a clean OS install.

### Mac OS X

1. Download the configuration files and include them in your Vim config:

	```bash
	git clone https://github.com/timkendrick/vim-quickstart.git
	echo "source $(pwd)/vim-quickstart/quickstart.vim" >> ~/.vimrc
	```

2. Install the [Vundle](https://github.com/VundleVim/Vundle.vim) package manager (used to install Vim plugins):

	```bash
	git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
	```

3. Install Vundle plugins:

	```bash
	vim -c PluginInstall -c bdelete -c quit
	```

4. Install required binaries:

	```bash
	brew install editorconfig
	brew install the_silver_searcher
	~/.vim/bundle/YouCompleteMe/install.py
	```

5. Install the [Powerline fonts](https://github.com/powerline/fonts/archive/master.zip)

6. Install MacVim (optional, but recommended):

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
| [unimpaired.vim](https://github.com/tpope/vim-unimpaired) | ✔︎ | ✔︎ | Paired action mappings |
| [surround.vim](https://github.com/tpope/vim-surround) | ✔︎ | ✔︎ | Wrap code blocks |
| [commentary.vim](https://github.com/tpope/vim-commentary) | ✔︎ | ✔︎ | Code commenting |
| [abolish.vim](https://github.com/tpope/vim-abolish) | ✔︎ | ✔︎ | Smart word substitution |
| [repeat.vim](https://github.com/tpope/vim-repeat) | ✔︎ | ✔︎ | Repeat complex actions |
| [vim-multiple-cursors](https://github.com/terryma/vim-multiple-cursors) | ✔︎ | ✔︎ | Sublime-style multiple cursors |
| [vim-expand-region](https://github.com/terryma/vim-expand-region) | ✔︎ | ✔︎ | Expand selection to parent block |
| [vim-textobj-user](https://github.com/kana/vim-textobj-user) | ✔︎ | ✔︎ | Custom text objects |
| [vim-textobj-lastpat](https://github.com/kana/vim-textobj-lastpat) | ✔︎ | ✔︎ | 'Last search pattern' text object |
| [vim-indent](https://github.com/timkendrick/vim-indent) | ✔︎ | ✔︎ | Convert between tabs and spaces |
| [DetectIndent](https://github.com/roryokane/detectindent) | ✔︎ | ✔︎ | Automatic indentation detection |
| [emmet-vim](https://github.com/mattn/emmet-vim) | ✔︎ | ✔︎ | Dynamic HTML snippets |
| [NERDTree](https://github.com/scrooloose/nerdtree) | | ✔︎ | File explorer sidebar |
| [nerdtree-git-plugin](https://github.com/Xuyuanp/nerdtree-git-plugin) | | ✔︎ | Git status in file explorer |
| [vim-gitgutter](https://github.com/airblade/vim-gitgutter) | | ✔︎ | Git status in gutter |
| [vim-airline](https://github.com/bling/vim-airline) | | ✔︎ | Improved status bar |
| [YouCompleteMe](https://github.com/Valloric/YouCompleteMe) | | ✔︎ | Code completion |
| [Syntastic](https://github.com/scrooloose/syntastic) | | ✔︎ | Syntax checking |
| [incsearch.vim](https://github.com/haya14busa/incsearch.vim) | | ✔︎ | Improved incremental search |
| [EditorConfig](https://github.com/editorconfig/editorconfig-vim) | | ✔︎ | [Editorconfig](http://editorconfig.org/) support |
| [ag.vim](https://github.com/rking/ag.vim) | | ✔︎ | Fast code search |
| [fugitive.vim](https://github.com/tpope/vim-fugitive) | | ✔︎ | Git repository actions |
| [vim-bufonly](https://github.com/schickling/vim-bufonly) | | ✔︎ | Allow closing all inactive buffers |
| [vim-colors-solarized](https://github.com/altercation/vim-colors-solarized) | | ✔︎ | [Solarized](http://ethanschoonover.com/solarized) color scheme |


## Included macros

| Macro | Terminal mode | GUI mode | Purpose |
| ----- | :-----------: | :------: | ------- |
| Matchit | ✔︎ | ✔︎ | Jump to block start/end |



## Keyboard mappings

| Keyboard shortcut | Action | Terminal mode | GUI mode |
| ----------------- | ------ | :-----------: | :------: |
| <kbd>Alt</kbd>+<kbd>v</kbd> | Paste from system clipboard | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>d</kbd> | Duplicate line | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>o</kbd> | Insert new line below cursor | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>o</kbd> | Insert new line above cursor | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>j</kbd> | Move line down | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>k</kbd> | Move line up | ✔︎ | ✔︎ |
| <kbd>Alt</kbd>+<kbd>t</kbd> | Create new buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>{</kbd> | Switch to previous buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>}</kbd> | Switch to next buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>w</kbd> | Close current buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>w</kbd> | Close all buffers except current buffer | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>s</kbd> | Save all buffers | | ✔︎ |
| <kbd>Alt</kbd>+<kbd>Tab</kbd> | Toggle NERDTree sidebar | | ✔︎ |

See plugin documentation for additional keyboard mappings.
