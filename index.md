---
title: vim / emacs keyboard shortcuts
---

# Keyboard shortcuts

## Navigation

| Navigation | vim   | emacs |
| ---------- | :---: | :---: |
| Goto line [count], default last line, on the first non-blank character linewise. | G | M-g g |
| Go to [count] Older cursor position in [jump list](#jumplist) | C-o | C-x C-SPC |
| Go to [count] newer cursor position in [jump list](#jumplist) | C-i | ? |
| Go to [count] older position in [change list](#changelist) | g; | ? |

## Buffers

| Buffers | vim   | emacs |
| ------- | :---: | :---: |
| Show all buffers | ls | C-x b |
| Unload buffer [N] (default: current buffer) and delete it from the buffer list | bdelete | C-x k |

## Editing

| Editing | vim   | emacs |
| ------- | :---: | :---: |
| Join [count] lines, with a minimum of two lines. Remove the indent and insert up to two spaces (see below). | J | M-^ |

# Glossary

## changelist

When making a change the cursor position is remembered.  One position is
remembered for every change that can be undone, unless it is close to a
previous change.

## jumplist

Jumps are remembered in a jump list.  With the CTRL-O and CTRL-I command you
can go to cursor positions before older jumps, and back again.  Thus you can
move up and down the list.  There is a separate jump list for each window. The
maximum number of entries is fixed at 100.

## vim definition of buffers and windows

- A buffer is the in-memory text of a file.
- A window is a viewport on a buffer.
- A tab page is a collection of windows.
