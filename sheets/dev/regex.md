# Regular expressions

## Commands

| Symbol | Description |
| ------ | ----------- |
|/ |start - end (we define a special character to put options behind, can also be: ', #, etc.) (standard is /) |
|^ |indicates the beginning of a string |
|$ |indicates the end of a string |
|\| |OR symbol |
|/string/i |option i = ignore case |
|/string/g |option g = global search : All matches (don't return after first match) |
|/string/m |option m = multiline search : Causes ^ and $ to match the begin/end of each line (not only begin/end of string) |
|[io] |“character class” in square brackets: one of the letters may be appropriate |
|- |"range of characters": ex: [a-z], [0-9], [a-z0-9], [a-zA-Z0-9] |
|^ (in a range of characters) |"exclusion" (eg: /[^0-9]/: we want at least one character different from a number)|
|? |"quantifier" => optional character (0 or 1 times), ex: /at?/ (=at{0,1}) |
|+ |"quantifier" => mandatory character (1 or more times), ex: /at+/ (=at{1,}) |
|* |"quantifier" => optional character (0, 1 or more times), ex: /at*/ (=at{0,}) |
|() |to make the quantifier apply to 2 or more letters, ex: /ch(at)*/ |
|. |matches any character except newline |
|\d |matches any digit (equivalent to [0-9]) |
|\w |matches any alphanumeric character or underscore (equivalent to [a-zA-Z0-9_]) |
|\s |matches any whitespace character (space, tab, newline) |
|\D, \W, \S |inverse of \d, \w, \s respectively |
|{n} |exactly n occurrences, ex: \d{3} |
|{n,m} |between n and m occurrences, ex: \d{2,4} |
|{n,} |at least n occurrences, ex: \d{2,} |
|\b |word boundary |
|\B |not a word boundary |


## Examples

Common regex patterns for validation:

For a URL:
```regex
^(https?|ftp):\/\/[^\s\/$.?#].[^\s]*$
```

For an email address:
```regex
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```

For a date in the format YYYY-MM-DD:
```regex
^\d{4}-\d{2}-\d{2}$
```

For an IPv4 address:
```regex
^(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)\.(25[0-5]|2[0-4][0-9]|[01]?[0-9][0-9]?)$
```


## Useful links
* [Regexp cheatsheet](https://devhints.io/regexp)
* [RegexOne](https://regexone.com)
* [RegExr](https://regexr.com)
* [Learn Regex - The easy way](https://github.com/ziishaned/learn-regex)
* [Regex101](https://regex101.com)
* [Regex Crossword](https://regexcrossword.com)
