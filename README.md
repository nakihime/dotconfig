# dotconfig
# Dot Config file for development env

Full and clean configurations for development environment on GNU Linux, macOS
and Cygwin.

## Prerequisite

- GNU Linux, macOS, Cygwin
- git, zsh, curl/wget
- Recommend: GNU Emacs, tmux
- Optional: Vim

## Quickstart

Run this command in the console.

``` shell
sh -c "$(curl -fsSL https://github.com/nakihime/dotconfig/raw/master/install.sh)"
```

or

``` shell
sh -c "$(wget https://github.com/nakihime/dotconfig/raw/master/install.sh -O -)"
```

## Docker

``` shell
cd ~/.dotfiles
docker build -t centaur/ubuntu .
docker run -it centaur/ubuntu zsh
```

## Shortcuts

- `Alt-c`: cd into the selected directory.
- `Ctrl-r`: Paste the selected command from history into the command line.
- `Ctrl-t`: Paste the selected file path(s) into the command line.
- `TAB`: To completions.

That's it. Enjoy!

## Customization

### ZSH ENV

Add your zsh environments in `~/.zshenv`. This is recommended by ZSH officially.
For example:

``` shell
export PATH=/usr/local/sbin:$PATH
export PATH=$HOME/.rbenv/shims:$PATH
export PYTHONPATH=/usr/local/lib/python2.7/site-packages
```

### ZSH local config

Set your personal zsh configurations in `~/.zshrc.local`. For example:

``` shell
# Oh-my-zsh plugin
zinit snippet OMZP::golang
zinit snippet OMZP::python
zinit snippet OMZP::ruby

# Github plugin
zinit light ptavares/zsh-direnv
```

See details on [zinit](https://github.com/zdharma-continuum/zinit).

### Git local config

Set your git configurations in `~/.gitconfig.local`, e.g. user credentials.

``` shell
[commit]
    # Sign commits using GPG.
    # https://help.github.com/articles/signing-commits-using-gpg/
    gpgsign = true

[user]
    name = John Doe
    email = john.doe@example.com
    signingkey = XXXXXXXX
```

## Screenshots

### Main (with Tmux)

![main](https://user-images.githubusercontent.com/140797/51855591-9717c880-2368-11e9-9270-bbadc3640982.png
"Main with tmux")

### Git Log

![git_log](https://user-images.githubusercontent.com/140797/51830877-cf4ce600-232b-11e9-9196-c35a59ebe491.png
" Git Log")

### [Centaur Emacs](https://github.com/seagle0128/.emacs.d)

![centaur_emacs](https://user-images.githubusercontent.com/140797/56488858-4e5c4f80-6512-11e9-9637-b9395c46400f.png
"Centaur Emacs")
