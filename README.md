zsh-vimode-visual
===

[![](https://img.shields.io/badge/powered%20by-zplug-ca7f85.svg?style=flat)](https://github.com/zplug/zplug)

`zsh-vimode-visual` provides visual mode in [Zsh Line Editer](http://zsh.sourceforge.net/Doc/Release/Zsh-Line-Editor.html)

## Description

[Zsh Line Editer](http://zsh.sourceforge.net/Doc/Release/Zsh-Line-Editor.html) has two vi-like editing mode (*viins*, *vicmd*), but Vim has three or more major editing mode such as *insert*, *command*, *visual* and so on. Let's implement visual mode in [Zsh Line Editer](http://zsh.sourceforge.net/Doc/Release/Zsh-Line-Editor.html).

![](https://raw.githubusercontent.com/b4b4r07/screenshots/master/zsh-vimode-visual/demo.gif)

## Installation

If you use [zplug](https://github.com/zplug/zplug) as a plugin manager for zsh, all you have to do is to put something like this to your `.zshrc`.

```zsh
zplug "b4b4r07/zsh-vimode-visual"
```

Also, if you want to use it without conflict with [`zsh-users/zsh-syntax-highlighting`](https://github.com/zsh-users/zsh-syntax-highlighting), please set as follows.

```zsh
zplug "zsh-users/zsh-syntax-highlighting", defer:2
zplug "b4b4r07/zsh-vimode-visual", defer:3
```

You can order the loading by setting the `defer` tag.
In addition, if the `defer` tag is set to 2 or more, it's load after running `compinit`.

Otherwise, to install manually:

```console
$ git clone https://github.com/b4b4r07/zsh-vimode-visual
$ source ./zsh-vimode-visual/zsh-vimode-visual.zsh
```

## Configuration

`zsh-vimode-visual` is implemented with ***vivis*** that emulates Vim visual mode and ***vivli*** mode.

```zsh
bindkey -M vicmd 'V'  vi-vlines-mode
bindkey -M vicmd 'v'  vi-visual-mode
bindkey -M vivis ' '  vi-visual-forward-char
bindkey -M vivis ','  vi-visual-rev-repeat-find
bindkey -M vivis '0'  vi-visual-bol
bindkey -M vivis ';'  vi-visual-repeat-find
bindkey -M vivis 'B'  vi-visual-backward-blank-word
bindkey -M vivis 'C'  vi-visual-substitute-lines
bindkey -M vivis 'D'  vi-visual-kill-and-vicmd
bindkey -M vivis 'E'  vi-visual-forward-blank-word-end
bindkey -M vivis 'F'  vi-visual-find-prev-char
bindkey -M vivis 'G'  vi-visual-goto-line
bindkey -M vivis 'I'  vi-visual-insert-bol
bindkey -M vivis 'J'  vi-visual-join
bindkey -M vivis 'O'  vi-visual-exchange-points
bindkey -M vivis 'R'  vi-visual-substitute-lines
bindkey -M vivis 'S ' vi-visual-surround-space
bindkey -M vivis "S'" vi-visual-surround-squote
bindkey -M vivis 'S"' vi-visual-surround-dquote
bindkey -M vivis 'S(' vi-visual-surround-parenthesis
bindkey -M vivis 'S)' vi-visual-surround-parenthesis
bindkey -M vivis 'T'  vi-visual-find-prev-char-skip
bindkey -M vivis 'U'  vi-visual-uppercase-region
bindkey -M vivis 'V'  vi-visual-exit-to-vlines
bindkey -M vivis 'W'  vi-visual-forward-blank-word
bindkey -M vivis 'Y'  vi-visual-yank
bindkey -M vivis '^M' vi-visual-yank
bindkey -M vivis '^[' vi-visual-exit
bindkey -M vivis 'b'  vi-visual-backward-word
bindkey -M vivis 'c'  vi-visual-change
bindkey -M vivis 'd'  vi-visual-kill-and-vicmd
bindkey -M vivis 'e'  vi-visual-forward-word-end
bindkey -M vivis 'f'  vi-visual-find-next-char
bindkey -M vivis 'gg' vi-visual-goto-first-line
bindkey -M vivis 'h'  vi-visual-backward-char
bindkey -M vivis 'j'  vi-visual-down-line
bindkey -M vivis 'jj' vi-visual-exit
bindkey -M vivis 'k'  vi-visual-up-line
bindkey -M vivis 'l'  vi-visual-forward-char
bindkey -M vivis 'o'  vi-visual-exchange-points
bindkey -M vivis 'p'  vi-visual-put
bindkey -M vivis 'r'  vi-visual-replace-region
bindkey -M vivis 't'  vi-visual-find-next-char-skip
bindkey -M vivis 'u'  vi-visual-lowercase-region
bindkey -M vivis 'v'  vi-visual-eol
bindkey -M vivis 'w'  vi-visual-forward-word
bindkey -M vivis 'y'  vi-visual-yank
```

## License

MIT [@b4b4r07](https://twitter.com/b4b4r07)
