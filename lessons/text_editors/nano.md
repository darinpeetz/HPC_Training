[![](../../Banner.jpg)](http://uwm.edu/hpc/support)

If you're looking to use Nano, it's probably because you need to do something simple and quick, and don't want to bother learning one of the more complex editors, so we'll cut to the chase.

### Starting Nano
You can start Nano one of two ways, by just typing the command `nano` to open a blank buffer, or by typing `nano /path/to/file` to open a buffer containing the contents of a particular file.

### Nano Shortcuts
Nano supports a wide variety of shortcuts to make editing files easier. A subset of these commands are usually displayed at the bottom of the editor. Keep in mind that the symbol `^` refers to the control key and `M-` refers to the meta key (which is usually `alt`). So for example `^G Get Help` means that typing `ctrl+g` opens a help menu. Note that while the uppercase letter is displayed, you'll need to enter the lowercase variant (don't press the shift key). If you don't want the commands displayed at the bottom of the window (e.g. if you prefer that extra space for editing), they can be turned off with the shortcut `alt+X`.

### Editing Contents
Nano is a WYSIWYG editor, so editing text is as simple as typing what you want. Keep in mind that you won't be able to use the mouse cursor to navigate around the file, you'll have to stick to using keyboard commands. The typical arrow keys, home/end, and page up/page down should work just fine if that's all you need; however, Nano also supports several shortcuts to help you move around the file quicker.

| Command | What it does |
| --- | --- |
| ctrl + F | Move cursor forward one space |
| ctrl + B | Move cursor backward one space |
| ctrl + P | Move cursor up one line |
| ctrl + N | Move cursor down one line |
| ctrl + A | Move cursor to start of line |
| ctrl + E | Move cursor to end of line |
| ctrl + Y | Move cursor up one page |
| ctrl + V | Move cursor down one page |
| ctrl + space | Move cursor forward one word |
| alt + space | Move cursor back one word |
| ctrl + _ | Prompt to move to (line, column) in buffer |

### Saving Your Edits
The shortcut for saving is `ctrl+O`. After entering the shortcut, a prompt will come up asking what file name to write to. If the buffer was initiated from an existing file (if you're editing a file rather than creating a new one), the prompt will auto-fill with the existing filename. Simply press enter to overwrite the file, or modify the filename to write to a new location.

If you try to close a buffer (`ctrl+X`) with unsaved edits, you will be prompted to save the changes before closing. If you choose to save, the same filename prompt will appear to ask where the file should be saved.

### Copying, cutting, and pasting
Since nano doesn't support the use of a mouse, it's necessary to use a shortcut command to highlight text for copying/cutting. Pressing `ctrl+^` followed by any navigation keys/shortcuts will highlight all text from the starting point up to (but not including) the final position of the cursor. From there `alt+^` will copy of the text or `ctrl+K` will cut it. As a side note, `ctrl+K` with no text highlighted will cut the line of text that the cursor is currently on.

You can paste text copied in this way by hitting `ctrl+U`. Note that this will only work for text copied/cut in Nano, if you copy something to the clipboard from another program (e.g. in a separate web browser), you cannot use `ctrl+U` to paste it. Instead use `shift+insert` to paste text from the clipboard.

### Searching
Use the shortcut `ctrl+W` to search for text in Nano. After entering the shortcut, type the text to search for followed by enter. To search for a second occurence, re-enter the shortcut and simply press enter (the default search phrase is the previously entered one). To change the search direction (forward or backward), enter `alt+B` after entering `ctrl+W`.

<br>
<table style="width:100%; border-collapse: collapse; border:0px solid black;" >
<tr style="border:0px solid black; border-top:1px solid #CCC; line-height:300%;">
<td style=" border:0px solid black; text-align:center; font-size:20px;"><a style="text-decoration:none;" href="./editors.html">Editors</a></td>
<td style=" border:0px solid black;"></td>
<td style=" border:0px solid black; text-align:center; font-size:20px;"><a style="text-decoration:none;" href="./editors.html">⬅ Editors</a></td>
<td style=" border:0px solid black; text-align:center; font-size:20px;"><a style="font-weight:bold;" href="./nano.html">Nano</a></td>
<td style="border:0px solid black; text-align:center; font-size:20px;"><a style="text-decoration:none;" href="./vim.html">Vim ➡</a></td>
