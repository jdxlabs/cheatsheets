# Regular expressions

## Commands

| Symbol | Description |
| ------ | ----------- |
|# |start - end (we define a special character to put options behind, can also be: ', /, etc.) |
|%%^%% |indicates the beginning of a string |
|$ |indicates the end of a string |
|%%|%% |OR symbol |
|#string#i |option i = ignore case |
|preg_match |PHP function: returns "true" if the regexp is checked, "false" otherwise (/!\ remember to tag its pattern: %%'#^pattern$#'%%) |
|[io] |“character class” in square brackets: one of the letters may be appropriate |
|- |"range of characters": ex: [a-z], [0-9], [a-z0-9], [a-zA-Z0-9] |
|%%^%% |in a range of characters: exclusion (eg: #[%%^%%0-9]#: we want at least one character different from a number)|
|? |"quantifier" => optional character (0 or 1 times), ex: #a?# (={0,1}) |
|+ |"quantifier" => mandatory character (1 or more times), ex: #a+# (={1,}) |
|* |"quantifier" => optional character (0, 1 or more times), ex: #a*# (={0,}) |
|() |to make the quantifier apply to 2 or more letters, ex: #Ay(ay)*# |

## Useful links
* [Regexp cheatsheet](https://devhints.io/regexp)
* [RegexOne](https://regexone.com)
* [RegExr](https://regexr.com)
* [Learn Regex - The easy way](https://github.com/ziishaned/learn-regex)
* [Regex101](https://regex101.com)
* [Regex Crossword](https://regexcrossword.com)
