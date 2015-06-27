# Vim

Vim is a text editor

## Modes

Vim has to modes insert mode and visual mode.
In insert mode you can insert text, append text and edit text
In visual mode you can mark a word, highlight, copy and paste, cut and paste, delete lines 'visually'

`i`   - start insert mode (insert befoe the cursor)
`v`   - start visual mode (mark line then do a command like y-yank)

`ESC` - Exit a mode

## Writing, Saving and Exiting

To write the file, save the file or exit the file you must first exit out of a mode using the `ESC` key

`:w`  - write, save the file without exiting
`:wq` - write and quit
`:x`  - write and quit
`ZZ`  - write and quit
`:q`  - quit (command will not be executed if there are unsaved changes)
`:!q` - quit and throw away any unsaved changes
`ZQ`  - quit and throw away any unsaved changes

## Cursor Movement

`h` - move cursor left
`l` - move cursor right
`j` - move cursor down
`k` - move cursor up

`w` - jump forward to the start of a word
`W` - jump forward to the start of a word that may or may not contain punctuation


