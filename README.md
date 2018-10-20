# cd-gitroot

## Synopsis
zsh plugin to change directory to git repository root directory

Inspired by [id:hitode909 blog post](http://hitode909.hatenablog.com/entry/20100211/1265879271).

## How to set up

### Manually install

Put git-root and _git-root files somewhere in your $fpath and add the following line to your .zshrc:

```
autoload -Uz git-root
```

#### For example

```
# download all files
% cd /path/to/dir
% git clone https://github.com/mollifier/cd-gitroot.git
```

And add the following lines to your .zshrc:

```
fpath=(/path/to/dir/cd-gitroot(N-/) $fpath)

autoload -Uz git-root
```

### Installing using Antigen
If you use [Antigen](https://github.com/zsh-users/antigen), add the following line to your .zshrc:

```
antigen bundle mollifier/cd-gitroot
```

### Installing using Zgen
If you use [zgen](https://github.com/tarjoilija/zgen), add the following to your `.zshrc`
```
zgen load mollifier/cd-gitroot
```
to your `.zshrc` with your other `zgen load` commands.

You can set alias to this function.
e.g.

```
alias cdu='git-root'
```

## Usage

```
git-root [PATH]
```

If PATH isn't specified, change directory to current git repository root directory.
else change directory to PATH instead of it.
PATH is treated relative path in git root directory.

## Options
\-h display help and exit
