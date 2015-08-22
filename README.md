# cd-gitroot

## Synopsis
cd-gitroot is a zsh plugin to change directory to a git repository's root directory

Inspired by [id:hitode909 blog post](http://hitode909.hatenablog.com/entry/20100211/1265879271).

## How to set up

### Manual install

Put cd-gitroot and _cd-gitroot files somewhere in your `$fpath` and add the following line to your `.zshrc`:

```
autoload -Uz cd-gitroot
```

#### For example

```
# download all files
% cd /path/to/dir
% git clone https://github.com/mollifier/cd-gitroot.git
```

Add the following lines to your `.zshrc`:

```
fpath=(/path/to/dir/cd-gitroot(N-/) $fpath)

autoload -Uz cd-gitroot
```

### Installing using Antigen
If you use the [Antigen](https://github.com/zsh-users/antigen) framework, add the following line to your .zshrc:

```
antigen bundle mollifier/cd-gitroot
```

### Installing with Zgen
If you're using [Zgen](https://github.com/tarjoilija/zgen) framework, add the following line to your `.zshrc` with your other plugins:

```
zgen load mollifier/cd-gitroot
```

You can set alias to this function.
e.g.

```
alias cdu='cd-gitroot'
```

## Usage

```
cd-gitroot [PATH]
```

If **PATH** isn't specified, change directory to the current git repository's root directory,
otherwise change directory to **PATH** inside of it.
**PATH** is treated as a path relative to the git root directory.

## Options
\-h display help and exit

