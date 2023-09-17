# Regular Expression Tutorial

A regular expression, often abbreviated as "regex", is a  pattern-matching language. Regex allows one to define a specific pattern or set of rules that can be used to validate strings or text data.



## Summary

The regular expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ is used to validate email addresses by checking whether an inputed string follows the specific pattern to form a valid email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)


## Regex Components

The regular expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ can be broken into four components: ^ and $, ([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}).

1. ^ and $ are anchors that go at the beginning and end of the text respectively

2. ([a-z0-9_.-]+) captures the part of the email before the @ symbol. "a-z" matches lowercase letters between a and z. "0-9" matches any digits. (_), (.), and (-), match any underscores, periods, and hyphens. (+) is for if any of these characters are used more than once.

3. ([\da-z.-]+) captures the domain after the @ symbol. "a-z" matches lowercase letters between a and z. "0-9" matches any digits. (_), and (.), match any underscores and periods.

4. ([a-z.]{2,6}) matches the TLD (top-level domain) (eg. the com in ".com"). "a-z" matches lowercase letters between a and z and (.), match any periods. {2,6} specifies that the preceding character class should occur between 2 to 6 times.


### Anchors

^ is the start anchor thats asserts that the match must start at the beginning of the text. The ^ ensures that the email address  begins with the pattern specified in the regular expression. Conversly, $ is the end anchor that ensures the end of the email address ends with the pattern specified in the regular expression.


### Quantifiers

+ and {2,6} are quantifiers that are used when issues of mulitplicity or character minimums and maximums arise. + is used to match one or more occurrences of the preceding element (if a character is repeated it will be ok). {2,6} means that this section of the pattern will have a minimum of 2 characters and a maximum of 6 characters.

### OR Operator

### Character Classes


### Grouping and Capturing

### Bracket Expressions


### Boundaries

/^ and $/ ensure that the regex is only the code inbetween.

## Author

My name is Noah Salmon. I am a student in a coding bootcamp. This is my GitHub: https://github.com/noahsalmon98

