
# Linux - `vi` command

## Shortcuts

### Cursor navigation

| Shortcut               | Action                                      |
| ---------------------- | ------------------------------------------- |
| **_Character_**        |                                             |
| `h`, `←`               | Cursor left                                 |
| `j`, `↓`               | Cursor down                                 |
| `k`, `↑`               | Cursor up                                   |
| `l`, `→`               | Cursor right                                |
| `l`, `→`               | Cursor right                                |
| _n_`\|`                | Go to _n_ th column                         |
| **_Text_**             |                                             |
| `w`, `b`, `e`          | Next/Previous/End word                      |
| `W`, `B`, `E`          | Next/Previous/End blank delimited word      |
| **_Line_**             |                                             |
| `0`, HOME              | Start of line                               |
| `$`, END               | End of line                                 |
| `^`                    | First char of line                          |
| `+`, `-`               | First char of next/previous line            |
| `H`                    | Move to top of screen                       |
| `M`                    | Move to middle of screen                    |
| `L`                    | Move to bottom of screen                    |
| n`H`, n`L`             | *n*th line from top/bottom of screen        |
| **_Scrolling_**        |                                             |
| `Ctrl-F`, `Ctrl-B`     | Scroll forward/backworkd one screen         |
| `Ctrl-D`, `Ctrl-U`     | Scroll forward/backworkd half screen        |
| `Ctrl-E`, `Ctrl-Y`     | Scroll forward/backworkd one line           |
| `z`(enter), `z.`, `z-` | Scroll current line to top/middle/bottom    |
| **_Search_**           |                                             |
| `/`pattern             | Search forward for pattern                  |
| `?`pattern             | Search backwoards for pattern               |
| `n`, `N`               | Go to next/previous match                   |
| `f`x, `F`x             | Find forward/backword for char x            |
| `;`, `,`               | Repeat current-line search forward/backword |
| `%`                    | Find matching `() {} []`                    |
| `*`                    | Find word under cursor                      |
| `:set ic / noic`       | Set case-sensitive on/off                   |
| **_Line Number_**      |                                             |
| `Ctrl-G`               | Display current line number                 |
| _n_`G`, `:`_n_         | Move to *n*th line                          |
| `1G`, `:1`, `gg`       | Move to first line of file                  |
| `G`, `:$`              | Move to last line of file                   |
| **_Marking Position_** |                                             |
| `m`x                   | Mark current position as x                  |
| `` ` ``x               | Move cursor to x                            |
| ` `` `                 | Return to previous mark                     |
| `'`x                   | Move to line containing mark x              |
| `''`                   | Return to line of previous mark             |

### Editing commands

| Shortcut                | Action                                                                          |
| ----------------------- | ------------------------------------------------------------------------------- |
| **_Insert_**            |                                                                                 |
| `i`, `a`                | Insert text before/after cursor                                                 |
| `I`, `A`                | Insert text at begining/end of current line                                     |
| `o`, `O`                | Insert text below/above current line                                            |
| **_Change_**            |                                                                                 |
| `r`                     | Replace with the next typed char                                                |
| `~`                     | Change char between uppercase/lowercase                                         |
| `c`_m_                  | Change text block defined by movement command _m_<br>Ex: `cw` changes next word |
| `cc`                    | Change current line                                                             |
| _n_`cc`, `c`_n_`c`      | Change next _n_ lines                                                           |
| `C`                     | Change to end of line                                                           |
| `R`                     | Type over characters                                                            |
| `s`                     | Substitute character and continue typing                                        |
| `S`                     | Substitute current line and continue typing                                     |
| **_Delete, Move_**      |                                                                                 |
| `x`, _n_`x`             | Delete 1/_n_ char (Del)                                                         |
| `X`, _n_`X`             | Delete back 1/_n_ chars (Backspace)                                             |
| `d`_m_                  | Delete text block defined by movement command _m_<br>Ex: `dw` deletes next word |
| `dd`                    | Delete current line                                                             |
| _n_`dd`, `d`_n_`d`      | Delete next _n_ lines                                                           |
| `D`                     | Delete to end of line                                                           |
| `p`, `P`                | Put deleted text before/after cursor                                            |
| **_Yank (copy/paste)_** |                                                                                 |
| `y`_m_                  | Copy text block defined by movement command _m_<br>Ex: `yw` yanks next word     |
| `yy`, `Y`               | Copy current line                                                               |
| _n_`yy`, `y`_n_`y`      | Copy next _n_ lines                                                             |
| `"`_a_`yy`              | Copy current line into buffer named _a_                                         |
| `p`, `P`                | Paste yanked text before/after cursor                                           |
| `"`_a_`P`               | Paste text from buffer _a_ after cursor                                         |
| **_Line_**              |                                                                                 |
| `J`                     | Join lines                                                                      |
| `<<`, `>>`              | Shift line left/right                                                           |
| **_Other Commands_**    |                                                                                 |
| `.`                     | Repeat last edit command                                                        |
| `u`                     | Undo last edit                                                                  |
| `U`                     | Undo changes to current line                                                    |
| `J`                     | Join two lines                                                                  |
| `Ctrl-L`, `Ctrl-R`      | Redraw/refresh screen                                                           |
| `ESC`                   | Exit insert mode lines                                                          |

### Ex commands

| Shortcut                                | Action                                                                        |
| --------------------------------------- | ----------------------------------------------------------------------------- |
| `:`_cmd_                                | Execute ex command _cmd_                                                      |
| `:` ↑ / ↓                               | Move up/down on the history of commands                                       |
| **_Range_**                             |                                                                               |
| _n_                                     | _n_ th line                                                                   |
| _n_`,`_m_                               | Lines from _n_ to _m_ line                                                    |
| `'`_a_                                  | line with mark _a_                                                            |
| `.`                                     | Current line                                                                  |
| `$`                                     | Last line                                                                     |
| `%`, `1,$`                              | All lines                                                                     |
| `-`_n_, `+`_n_                          | Previous/next _n_ th line                                                     |
| **_File Commands_**                     |                                                                               |
| `:w`                                    | Save file                                                                     |
| `:w` _filename_                         | Save file as _filename_                                                       |
| `:[range] w` _filename_                 | Save lines in _range_ to _filename_                                           |
| `:r` _filename_                         | Insert content of _filename_ at cursor position                               |
| `:e`                                    | Reload file                                                                   |
| `:e!`                                   | Discard changes and reload file                                               |
| `:set autoread`                         | Enable auto read                                                              |
| **_Quit Commands_**                     |                                                                               |
| `:q`                                    | Quit                                                                          |
| `ZZ`, `:x`, `:wq`                       | Save file and quit                                                            |
| **_Shell Commands_**                    |                                                                               |
| `:!`_cmd_                               | Execute shell command _cmd_                                                   |
| `:sh`                                   | Open shell                                                                    |
| **_Find & Replace Command_**            |                                                                               |
| `:[range] s/{pattern}/{string}/[flags]` | Find and replace {pattern} with {string}                                      |
| `:s/{pattern}/{string}`                 | Find and replace first {pattern} with {string} in current line                |
| `:s/{pattern}/`                         | Find and replace first {pattern} empty string                                 |
| `:s//{string}`                          | Find and replace last searched {pattern} with {string}                        |
| `:s/{pattern}/{string}/g`               | Find and replace all {pattern} with {string} in current line                  |
| `:1,5 s/{pattern}/{string}/g`           | Find and replace {pattern} with {string} in lines 1 to 5                      |
| `:% s/{pattern}/{string}/gc`            | Find and replace {pattern} with {string} in all file, asking for confirmation |
| **_Replace_**                           |                                                                               |
| `\&`, `\0`                              | Replace with matched text                                                     |
| `\`_n_                                  | Replace with _n_ th group                                                     |
| **_Flag_**                              |                                                                               |
| `g`, `c`, `i`, `I`                      | Global / Confirm / Case-insensitive / Case-sensitive                          |

### Options

| Shortcut                  | Action                                |
| ------------------------- | ------------------------------------- |
| `:set`                    | Show current options                  |
| `:set all`                | Show all options                      |
| `:set `_option_           | Enable _option_. Ex: `:set number`    |
| `:set no`_option_         | Disable _option_. Ex: `:set nonumber` |
| `:set `_option_`=`_value_ | Set _option_ _value_                  |
| `:set `_option_`?`        | Show _option_ value                   |
| **_Common Options_**      |                                       |
| `number / nu`             | Show line number                      |
| `wrap`                    | Warp line                             |
| `ignorecase / ic`         | Ignore case during search             |
| `autoread`                | Watch file                            |

## Reference

- [Vi Editor Cheat Sheet (PDF)](https://www.cse.scu.edu/~yfang/coen11/vi-CheatSheet.pdf)

### Tags

`#linux #bash #shell #vi #vim`
