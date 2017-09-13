---
title: index
---

# Navigation keyboard shortcuts

| Navigation | vim   | emacs |
| ---------- | :---: | :---: |
| Goto line [count], default last line, on the first non-blank character linewise. | G | M-g g |
| Join [count] lines, with a minimum of two lines. Remove the indent and insert up to two spaces (see below). | J | M-^ |
| Go to [count] Older cursor position in [jump list](#jumplist) | C-o | C-x C-SPC |
| Go to [count] newer cursor position in [jump list](#jumplist) | C-i | ? |
| Go to [count] older position in [change list](#changelist) | g; | ? |
| Show all buffers | ls | ? |
| Unload buffer [N] (default: current buffer) and delete it from the buffer list | bdelete | ? |

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
