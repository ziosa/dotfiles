# My dotfiles

Based on [Mathias](https://github.com/mathiasbynens/dotfiles) ones.

Please refer to his documentation for more details.

## Installation

You can clone the repository wherever you want. (I like to keep it in `~/dotfiles`, with `~/dotfiles` as a symlink.) The bootstrapper script will pull in the latest version and copy the files to your home folder.


	git clone https://github.com/vesparny/dotfiles.git && cd dotfiles && source bootstrap.sh


### `.path`

If `~/.path` exists, it will be sourced along with the other files

Here’s an example `~/.path`:

	#give brew priority on other binaries
	PATH=/usr/local/bin:/usr/local/sbin:${PATH}
	#something else
	PATH=$PATH:~/code/git-friendly
	...
	exoprt PATH

### `.extra`

If `~/.extra` exists, it will be sourced along with the other files. You can use this to add a few custom commands without the need to fork this entire repository, or to add commands you don’t want to commit to a public repository (Like git user and email)

### `.functions`

Useful functions like:

* encrypt
* decrypt
* ...

### `.aliases`

Useful aliases like:

* secureEmptyTrash
* emptyTrash
* ...

### `.vimrc`

vim config.


### Sensible OS X defaults

When setting up a new Mac, you may want to set some sensible OS X defaults:

	./.osx

### Install Homebrew formulae

When setting up a new Mac, you may want to install some common [Homebrew](http://brew.sh/) formulae (after installing Homebrew, of course):

	brew bundle ~/Brewfile

### Install native apps with `brew cask`

You could also install native apps with [`brew cask`](https://github.com/phinze/homebrew-cask):

	brew bundle ~/Caskfile


### `init/` folder

### TODO

* review of `.editorconfig`, `Brewfile`, `Caskfile`
* track basic nodejs -g packages (Like httpster)
* add sublime shortcuts
* install quicklook plugins
