# apt-vim
Advanced Packaging Tool for VIM

Summary
-------------
apt-vim aims to serve as a complete VIM plugin management tool including dependency installation, using [Pathogen](https://github.com/tpope/vim-pathogen) at its core to load plugins. Plugins, and their dependencies, can be installed, removed, and updated using this one tool.

Plugin installation recipes can be saved and shared, allowing users to create portable configuration files, and allowing plugin developers to create an automated installation process for their users.

Installation
------------
1. Install VIM
2. Install Git
3. Install python 2.7.x
4. Clone this repo:  `git clone https://github.com/egalpin/apt-vim.git`
5. Add `apt-vim` to you `PATH` for ease of use:  `sudo cp apt-vim /usr/local/bin`
6. Add `execute pathogen#infect()` and then `call pathogen#helptags()` to `~/.vimrc`
  - If `~/.vimrc` doesn't exist, create a new file containing just the above 2 commands
7. Run `apt-vim init`
8. Add `~/.vimpkg/bin` to your `PATH`
  - `export PATH=$PATH:~/.vimpkg/bin`
  - This is where all Vim plugin dependencies will be installed
9. Run `apt-vim install -y`
  - This will clone and install [Pathogen](https://github.com/tpope/vim-pathogen) and, as an example, [Tagbar](https://github.com/majutsushi/tagbar) and its dependency, `ctags`
