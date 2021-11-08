# `ZSH-MORPHO`

## Introduction

Terminal screen saver for Zshell. Implements morphogenesis and Mandelbrot
images. Written in pure Zshell (possible thanks to floating point numbers
and to `zsh/mathfunc` module). Supports running external commands, for
example `cmatrix`.

Screen saver will start after configured time, in last terminal in which
a command has been executed.

Video – view on [asciinema](https://asciinema.org/a/47242). You can resize the video by pressing `Ctrl-+` or `Cmd-+`.

[![asciicast](https://asciinema.org/a/47242.png)](https://asciinema.org/a/47242)

## Configuration

There are 4 zstyles:

```zsh
zstyle ":morpho" screen-saver "zmorpho" # select screen saver "zmorpho"; available: zmorpho, zmandelbrot, zblank, pmorpho
                                        # this  can also be a command, e.g. "cmatrix"
zstyle ":morpho" arguments "-s"         # arguments given to screen saver program; -s - every key press ends
zstyle ":morpho" delay "290"            # 5 minutes before screen saver starts
zstyle ":morpho" check-interval "60"    # check every 1 minute if to run screen saver
```

To test screen savers run them directly from command line, e.g. issue "`pmorpho`".

## Installation

The plugin is "standalone", which means that only sourcing it is needed. So to
install, unpack `zsh-morpho` somewhere and add
`source {where-zsh-morpho-is}/zsh-morpho.plugin.zsh` to `zshrc`.

If using a plugin manager, then `Zinit` is recommended, but you can use any
other too, and also install with `Oh My Zsh` (by copying directory to
`~/.oh-my-zsh/custom/plugins`).

### [Zinit](https://github.com/z-shell/zinit)

Add `zinit load z-shell/zsh-morpho` to `.zshrc`.
The plugin will be loaded next time you start `Zsh`.
To update issue `zinit update z-shell/zsh-morpho` from command line.

### Zgen

Add `zgen load z-shell/zsh-morpho` to `.zshrc` and issue a `zgen reset` (this
assumes that there is a proper `zgen save` construct in `.zshrc`).

### Antigen

Add `antigen bundle z-shell/zsh-morpho` to `.zshrc`. There also should be
`antigen apply`.

### Oh-My-Zsh

1. `cd ~/.oh-my-zsh/custom/plugins`
2. `git clone https://github.com/z-shell/zsh-morpho.git`
3. Add `zsh-morpho` to your plugin list
