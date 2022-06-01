# What is a regex

In this short markdown I will be explaining what a regex is and how it works.

## Summary

A regex is short for regular expression and is a pattern that makes sure that the characters within a string match certain perameters.
As an example I will be using this password regex to demonstrate.

`^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*#?&])[A-Za-z\d@$!%*#?&]{8,}$`

## Table of Contents

- [What is a regex](#what-is-a-regex)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [Grouping Constructs](#grouping-constructs)
    - [Bracket Expressions](#bracket-expressions)
    - [Character Classes](#character-classes)
    - [The OR Operator](#the-or-operator)
    - [Flags](#flags)
    - [Character Escapes](#character-escapes)
  - [Author](#author)


## Regex Components
There are many regex components but the ones that we will talk about today are anchors, quanitifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags, and character escapes.
### Anchors
Anchors are the symbols that are on the end of the regex. In our regex
`^` and `$` are the anchors. The following are anchors and here is what they do.

`^: Beginning of string (or line, depending on the mode)`

`$: End of string (or line, depending on the mode)`

`\A: Beginning of string`

`\z: End of string`

`\Z: Varies a lot depending on the engine, so be careful with it`

`\b: Word boundary`

`\B: Not a word boundary`

Source: https://cs.lmu.edu/~ray/notes/regex/
### Quantifiers
Quantifiers show the necessary quantity of a certain group of characters. In our regex the end has `{8,}` which means that the password must have at least 8 characters in total.
### Grouping Constructs
Different groups of characters can be split up in the regex. In our example the regex has 

`^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*#?&])[A-Za-z\d@$!%*#?&]{8,}$`

The first group must be true before the regex can move on to the next group.
### Bracket Expressions
Bracket expressions contain characters that the string can have for example the first bracket expression in the password check is `[A-Za-z]` which checks for uppercase letters from A to Z and then does the same for lowercase. Square brackets also look for exactly one character.
### Character Classes
Brackets look for exactly one character but there are other ways to do this as well.

`\d             [0-9]`

`\D             [^\d]`

`\s             [ \t\n\x0B\f\r]`

`\S             [^\s]`

`\w             [a-zA-Z0-9_]`

`\W             [^\w]`

`.              any character at all, except maybe not a line terminator`

Source: https://cs.lmu.edu/~ray/notes/regex/
### The OR Operator
The or operator is reperesented as `|`. Our current example does not use this but it is quite simple to explain with another regex snippet.

`black|white|blue|red|green`

This snippet of a regex would look for the colors black, or white, or blue, or red, or green. 
### Flags
Flags are used after slashes in a regex to make the regex search through in a different way. Our regex uses `/d` which looks for one number between 0 and 9 and is the same as `[0-9]`.
### Character Escapes
Character escapes help you to get out of literal characters so that things such as a space with `\s` or a word with `\w`. Our password uses `\d`  which is a number between 0 and 0.
## Author
I am Brant Martin, I like videothis is my GitHub.

https://github.com/BrantMartin