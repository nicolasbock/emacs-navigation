---
title: editor comparison
---

# Keyboard shortcuts

## Navigation

| Navigation | vim   | emacs |
| ---------- | :---: | :---: |
| Goto line [count], default last line, on the first non-blank character linewise. | `G` | `M-g g` |
| Go to [count] Older cursor position in [jump list](#vim-jumplist) | `C-o` | `C-x C-SPC` |
| Go to [count] newer cursor position in [jump list](#vim-jumplist) | `C-i` | ? |
| Go to [count] older position in [change list](#vim-changelist) | `g;` | ? |
| Find the next item in this line after or under the cursor and jump to its [match](#vim-match-motion) | `%` | ? |
| Display error [nr] in the [quickfix list](#vim-quickfix-list) | `:cc` | ? |
| Display the [count] next error in the [quickfix list](#vim-quickfix-list) | `:cn` | ? |
| Display the first error in the [count] next file in the [quickfix list](#vim-quickfix-list) | `:cnf` | ? |

## Buffers

| [Buffers](#vim-definition-of-buffers-and-windows) | vim   | emacs |
| ------- | :---: | :---: |
| Show all buffers | `ls` | `C-x b` |
| Unload buffer [N] (default: current buffer) and delete it from the buffer list | `bdelete` | `C-x k` |

## Editing

| Editing | vim   | emacs |
| ------- | :---: | :---: |
| Join [count] lines, with a minimum of two lines. Remove the indent and insert up to two spaces (see below). | `J` | `M-^` |
| Repeat last change [[1](http://vimdoc.sourceforge.net/htmldoc/repeat.html#single-repeat)] | `.` | `dot-mode` [[2](https://www.emacswiki.org/emacs/dot-mode.el)] |

## Packages

| vim | emacs |
| --- | ----- |
| `fugitive` | `magit` |
| `command-t` | `flx`, `ido-mode` |

# Glossary

## vim changelist

When making a change the cursor position is remembered.  One position is
remembered for every change that can be undone, unless it is close to a
previous change.

## vim jumplist

Jumps are remembered in a jump list.  With the CTRL-O and CTRL-I command you
can go to cursor positions before older jumps, and back again.  Thus you can
move up and down the list.  There is a separate jump list for each window. The
maximum number of entries is fixed at 100.

## vim definition of buffers and windows

- A buffer is the in-memory text of a file.
- A window is a viewport on a buffer.
- A tab page is a collection of windows.

## vim match motion

Find the next item in this line after or under the cursor and jump to its
match.

Items can be:

- `([{}])`

    parenthesis or (curly/square) brackets
- `/* */`

    start or end of C-style comment
- `#if`, `#ifdef`, `#else`, `#elif`, `#endif`

    C preprocessor conditionals (when the cursor is on the # or no ([{
    following)

## vim quickfix list

Vim has a special mode to speedup the edit-compile-edit cycle.  This is
inspired by the quickfix option of the Manx's Aztec C compiler on the Amiga.
The idea is to save the error messages from the compiler in a file and use Vim
to jump to the errors one by one.  You can examine each problem and fix it,
without having to remember all the error messages.

# References

[1] http://vimdoc.sourceforge.net/htmldoc/repeat.html#single-repeat

[2] https://www.emacswiki.org/emacs/dot-mode.el
