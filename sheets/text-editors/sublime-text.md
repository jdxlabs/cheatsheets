# Sublime Text 3

## Shortcuts
| Command | Shortcut | Shortcut 2 |
| ------- | -------- | ---------- |
| Next file | Ctrl+PageUp | |
| Previous file | Ctrl+PageDown | |
| Next file in history | Ctrl+Tab | |
| Previous File in History | Ctrl+Shift+Tab | |
| Move selection up | Ctrl+Shift+Up | |
| Move Selection Down | Ctrl+Shift+Down| |
| Toggle how | Ctrl + / | |
| Toggle block comment | Ctrl + Shift + / | |
| New file | CTRL+n | |
| Undo | CTRL+z | |
| Redo | ctrl+y | |
| Search | CTRL+f | |
| Search Next | F3 | |
| Search previous | Shift+F3 | |
| Go to desired line | Ctrl+g | |
| Jump to the corresponding brace of a function | CTRL+m | |
| Align lines by one character | Ctrl+Alt+a | |
| Vertical selection | Shift + right click | |
| Duplicate line | Ctrl+Shift+d | |
| Delete line | Ctrl+Shift+k | |
| Upper case | Ctrl+k, Ctrl+u | |
| lowercase | Ctrl+k, Ctrl+l | |
| File list | CTRL+p | |
| Shortcut list | Ctrl+Shift+p | |
| List functions | CTRL+r | |

## Install packages
To install and manage its packages, it is recommended to [[http://wbond.net/sublime_packages/package_control/installation|install Package Control]].

Then go to: Preferences -> Package Control -> Install/Remove Package.

Interesting packages:
   * Alignment
   * FileDiffs
   * SFTP

## Install syntax highlighting
I made this package, inspired by the Nexus theme: [[https://github.com/jdxlabs/darkgarden-theme-sublimetext|Colorscheme DarkGarden]].

## Settings - User
```bash
{
"color_scheme": "Packages/Color Scheme - Default/Mariana.sublime-color-scheme",
"default_line_ending": "unix",
"font_face": "DejaVu Sans Mono",
"font_size": 12,
"highlight_modified_tabs": true,
"open_files_in_new_window": false,
"scroll_speed": 0,
"theme": "Adaptive.sublime-theme",
"translate_tabs_to_spaces": true,
"trim_trailing_white_space_on_save": true,
"find_selected_text": true,
"update_check": false
}

```

