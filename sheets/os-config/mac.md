# Some configuration tips for Mac OS X

## Software
You can find a list of tools to work under Mac OS X on the [[software-equivalents|Software equivalents]] page.

## Keyboard shortcuts for Macbook Pro
| Action                     | Shortcut    |
| -------------------------- | ----------- |
|Finder : Go to                                  |⌘ + ⇧ + g      |
|Finder : Show hidden files                      |⌘ + ⇧ + .      |
|Finder : Show file infos                        |⌘ + i           |
|Finder : Show multiple files infos              |⌘ + ⌥ + i      |
|Keyboard : "["                                  |⌥ + ⇧ + (      |
|Keyboard : "]"                                  |⌥ + ⇧ + )      |
|Keyboard : <nowiki>"|"</nowiki>                 |⌥ + ⇧ + l      |
|Keyboard : "~"                                  |⌥ + n           |
|Keyboard : "{"                                  |⌥ + (           |
|Keyboard : "}"                                  |⌥ + )           |
|Keyboard : "\"                                  |⌥ + ⇧ + /      |
|Keyboard : Page Up                              |fn + up         |
|Keyboard : Page Down                            |fn + down       |
|Keyboard : Home                                 |fn + left       |
|Keyboard : End                                  |fn + right      |
|Screen capture                                  |⌘ + ⇧ + 3      |
|Screen capture with selection                   |⌘ + ⇧ + 4      |

## Legend for mac shortcuts
  * Command ⌘
  * Shift ⇧
  * Option ⌥
  * Control ⌃
  * Caps Lock ⇪
  * Fn

## VirtualBox shortcuts compatibility
  * Add a keyboard -> France  -> France Apple Macintosh
  * Use right Cmd as Host key
(Tested on a Macbook Pro with a Debian image)

## View the hidden files in the Finder
```bash
defaults write com.apple.Finder AppleShowAllFiles -boolean TRUE
killall Finder
```


## Speed up the dock auto-hide
```bash
defaults write com.apple.dock autohide-delay -float 0
defaults write com.apple.dock autohide-time-modifier -float 0.4; killall Dock
```
