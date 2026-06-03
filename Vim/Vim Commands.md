<br>


- `i`   for insert mode
- `A`  for insert mode that starts at the end of the line
- `0`  will bring you to the beginning of a line in  normal mode
- `$`  will bring you to the end of the line in normal mode
- `u`  will undo the last change made in normal mode
- `:q` us to quit using command mode
- `:w` will save the file and can be combined with q.
- `:q!` adding the ! with q will exit the file without making any changes  

***  

- a buffer is similar to an open file
- `x` will delete a character in normal mode
- `dd` will delete a line in normal mode 
- `h` to move the cursor left in normal mode
- `j` to move the cursor left in normal mode
- `k` to move the cursor up in normal mode
- `l` to move the cursor right in normal mode
- `:r` for will open up another file inside the current file you are viewing in command mode.
- `:!` will run linux command inside vim  

***  

- `:e`  (edit) opens a new buffer in its own window in command mode.
- `:bp` (buffer previous) will switch to the original file opened in command mode.
- `:bn` (buffer next) will switch to the next file that is opened.
- `:enew` will open a new empty buffer.
- `bd` (buffer delete) will close a open buffer.  

***  

- `v`  for visual mode
- `y` (yank) will copy the highlighted text.
- `p` (out) will paste the copied text on a new line.
- `:`  when using visual mode and typing `sort ui` un the prompt will alphabetize the highlighted text
- `:%s/text1/text2/g` this will find and replace text in the file in command mode.
- `gg` will move to the top of the file in normal mode
- `G` (shift + g ) will move to the end of the file in normal mode.