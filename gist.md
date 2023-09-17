# Regular Expression Tutorial

A regular expression, often abbreviated as "regex", is a  pattern-matching language. Regex allows one to define a specific pattern or set of rules that can be used to validate strings or text data.



## Summary

The regular expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ is used to validate email addresses by checking whether an inputed string follows the specific pattern to form a valid email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)
- [Author] (#author)



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

### Character Classes

*[a-z0-9_.-]: a through z (all lowercase letters), 0 through 9 (all digits), _ (underscore), . (period), - (hyphen)

*[\da-z.-]: a through z (all lowercase letters), 0 through 9, (all digits), . (period), - (hyphen)

*[a-z.]: a through z (all lowercase letters), . (period)


### Grouping and Capturing

This regular expression is made up of three groups:

1. ([a-z0-9_.-]+), matches one or more lowercase letters between a-z, numbers between 0-9, underscores, periods, and hyphens. The expression is then followed by an @ sign.

2. ([\da-z.-]+) - the domain name must be matched which can use one or more digits, letters between a-z, periods, and hyphens. The domain name is then followed by a period.

3. ([a-z.]{2,6}) - matches the TLD. This section looks for any group of letters or dots that are 2-6 characters long.

### Bracket Expressions

*[a-z0-9_.-], matches characters in the part of the email address before the "@" symbol
*[\da-z.-], matches characters in the part of the email address after the "@" symbol, before the "."
*[a-z.], matches any lowercase letter (a-z) or a period (.) within the TLD

### Boundaries

/^ and $/ ensure that the regex is only the code inbetween.

## Author

My name is Noah Salmon. I am a student in a coding bootcamp. This is my GitHub: https://github.com/noahsalmon98

