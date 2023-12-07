# Vim

## Shortcut List

<sortable 1>
^command ^ shortcut ^ shortcut 2 ^
| BufferList | F1 | |
| Show File Explorer (NerdTree) | F3 | |
| Show function explorer (TagList) | F4 | |
| Force Vim to terminate | :q! | |
| Discard changes and reload file | :e! | |
| Exit Vim without saving changes | :q | |
| Replace file "file" | :w! file | |
| Save file | :w | |
| Save file and quit Vim | :wq | |
| Save file as "file" | :w file | |
| Buffer Next | :bn | tab |
| Buffer Previous | :bp | CTRL+TAB |
| Buffer <buffer number> | :b<buffer number> | |
| Show all buffers and their numbers | :buffers | |
| Show help on a command | :help <command> | |
| Split screen horizontally | Ctrl+w n | :sp |
| Move between viewports | Ctrl+w <direction> | |
| New file | :e <filename> | |
| Undo | u | |
| Redo | CTRL+r | |
| Search | /<search> | |
| Search Next | n | |
| Search previous | N | |
| Remove overline from search phrase | :no | F2 |
| Cut | d | |
| Copy (yank) | y | |
| Paste | P | |
| Cut Line | dd | |
| Copy line | yy | |
| Paste line | pp | |
| Visual Mode | Shift+v | |
| Go to top of file | gg | |
| Go to bottom of file | G | |
| Crop screen vertically | :vsp | |
| Exit current viewport | Ctrl+wq | |
| Delete current buffer | :bd | |
| Launch an internal command | :!<command> | |
| Return to last edited file | CTRL+6 | CTRL+ |
| Search - Replace (with confirmation) | :%s /find/replace/cg | |
| Jump to the corresponding brace of a function | % | |
| Comment code | ,cc | ,cs |
| Uncomment code | ,cu | |
| Navigate from one word to another in a text | Shift+right (or left) | |
| Go to desired line | <line_num>G | <line_num>gg |
| Complete a word | insert mode:Ctrl+N | |
| Complete PHP code | insert mode:Ctrl+X Ctrl+O | |
| Insert file path | mode insert:\fp | |
| Insert file name | mode insert:\fn | "%p |
| Align lines by one character | :Align <char> | |
| Reload File | :edit | :e |
| Vertical selection | Ctrl+v | CTRL+q |
| Lowercase a line | guu | |
| Capitalize a line | gUU | |
| Reindent File | G=gg | |
| Move word by word to the right | w | Ctrl+right |
| Move left word by word | b | Ctrl+left |
| Switch to last used buffer | :b# | |

</sortable>

## Configuration

I made a configuration with some plugins, [[https://github.com/jdxlabs/config-vim|available here]], you can make your own, inspiring yourself.

## List of commands

<sortable 1>
^command ^ command ^ command 2 ^
| Enable/Disable Word Wrap | :set wrap | :set nowrap |
| Change file encoding | :set fileencoding=... | |
| Change file format | :set fileformat=... | |
| Plugin: Buffer Explorer | , be | |
</sortable>


## Vertical Selection Tip

To edit multiple lines: \\
Ctrl+Shift+v and select the different lines, \\
Shift+i and write the desired text, \\
ESC when finished, \\

To delete characters on multiple lines: \\
Ctrl+Shift+v and select the characters of the different lines, \\
X to remove characters, \\
ESC when finished, \\


## Useful links
  * [[https://learnvim.irian.to/|Learn Vim - The Smart Way]]
  * [[https://realpython.com/vim-and-python-a-match-made-in-heaven/|VIM and Python – A Match Made in Heaven]]



