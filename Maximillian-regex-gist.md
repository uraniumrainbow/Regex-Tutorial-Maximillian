# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/

Anchors include the `^` at the beginning, telling the program where to begin, and the `$` at the end, signalling where to end. These are merely guideposts and do not signify matches of any characters.

### Quantifiers

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

Quantifiers limit what a given string can contain. 
The `+` signifies that the string must contain at least one character from the sequence it is contained in; in this case, the first `+` requires at least one character from `[a-z0-9_\.-]`. The `{2-6}` are bracket quantifiers that set a range on how many times a character must be used (in this case, no fewer than 2, no more than 6).

### OR Operator

OR operatiors are marked with `|` and indicates a choice of one of multiple options. It is often framed in situations like `{option1|option2}`

### Character Classes

Character classes are often depicted as a frontslash plus a single character, such as:
`\d`: 'digit,' [0-9]
`\w`: `[a-zA-Z0-9_]` a shortcut for all letters and numbers.

### Flags

Flags are amendments to the default behaviour of a Regex string search. For instance:

`i`: Ignore casing-- normally, the strings `abc` & `ABC` would be different, but under the `i` flag, they would both be included in a search.

`g`: Global-- searches everywhere on the machince for related Regex

### Grouping and Capturing

Grouping refers to the use of `()`to include multiple character specifications in one statement, such as in `(`[\da-z\.-]+`)`. This results in a unique Capture that will be stored in memory.

### Bracket Expressions

A bracket expression represents a list of specific characters one might wish to match, such as `[0-9]` or `[a-zA-Z]`

### Greedy and Lazy Match

A greedy match, like Regex, will attempt to match any occurance of an input possible. For instance, the use of `*` in an expression will result in an attempt to get as much of a match as possible, including partials, single characters, full list of strings, etc. Conversely, the `?` character will perform a lazy match, finding the least matches possible.

### Boundaries

Boundaries, denoted with `\b`, are used to capture specific instances within a string. For instance, the term `\bear\b` will search and find "lend me an `ear`" but not "t`ear`ing up."

### Back-references

A back-reference is a means of matching the same text as a previously matched capturing group. Start indexing from `\1` to find the single previous mention, and so on.

### Look-ahead and Look-behind

Look-behind `?<=` indicates a result after a specified sentence. For instance, the search `(?<=I am).*` in a text containing `I am hungry` will return `hungry` since it's behind the specified string. Conversely, look-ahead will pull results from ahead of the specified string.

## Author

Maximillian Doren is a student of the University of Utah Full-Stack Web Developer Bootcamp. Github: https://github.com/uraniumrainbow
