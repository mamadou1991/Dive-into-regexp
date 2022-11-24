# Title (Dive-into-regexp)

## Summary

Regular expressions are used to extract information by matching search patterns.

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
Regex components are differents characters that are combined to make the search.

### Anchors
Anchors are characters that matches the beginning and the end of end of a string.
^The matches any string that starts with The. 
Example: ^The/g
^ asserts position at start of the string
The matches the characters The literally (case sensitive).
end$ matches a string that ends with end^.
Example: /end$/g.
The end matches the characters end literally (case sensitive)
$ asserts position at the end of the string, or before the line terminator right at the end of the string (if any)


### Quantifiers
Quantifiers defines how many instances of a character, group, or character class must be in the input for a match to be found.

Example:

*	*?	Matches zero or more times.
+	+?	Matches one or more times.
?	??	Matches zero or one time.
{ n }	{ n }?	Matches exactly n times.
{ n ,}	{ n ,}?	Matches at least n times.
{ n , m }	{ n , m }?	Matches from n to m times.


### OR Operator
The OR operator are used to match to match one or several pattern separated by the '|' character.
Example:
a(b|c) matches a string that has a followed by b or c (and captures b or c).


### Character Classes
The character classes matches a single character from a group of Characters.
Examples:
 \d matches a single character that is a digit: 
a2b, a42c.
\w matches a word character (alphanumeric character plus underscore):
a2b, a42c.

### Flags
They modified the search.
Examples: 
‘i’perform a case-insensitive search.
m :(multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string.
g: performs a global search.



### Grouping and Capturing
They modified the search.
Examples: 
‘i’perform a case-insensitive search.
m :(multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string.
g: performs a global search.


### Bracket Expressions
Braket expressions are used to match a single character from a list of characters.
Examples:
|`(abc)`| matches a single character `a`, `b`, or `c`.
[a-fA-F0-9]
Match a single character present in the list above.
a-f matches a single character in the range between a (index 97) and f (index 102) (case sensitive)
A-F matches a single character in the range between A (index 65) and F (index 70) (case sensitive)
0-9 matches a single character in the range between 0 (index 48) and 9 (index 57) (case sensitive)

### Greedy and Lazy Match
Greedy and lazy match are regular expressions that expand the match as far as they can through the provided text.
Examples:
<.*?>/g
< matches the character < with index 6010 (3C16 or 748) literally (case sensitive)
. matches any character (except for line terminators)
*? matches the previous token between zero and unlimited times, as few times as possible, expanding as needed (lazy)
>
 matches the character > with index 6210 (3E16 or 768) literally (case sensitive).

### Boundaries
Boundaries matches positions where one side is a word character (like \w) and the other side is not a word character .
Examples:\Babb\B/g
\B : assert position where \b does not match
abb: matches the characters abb literally (case sensitive)
\B: assert position where \b does not match
### Back-references
Backreferences match the same text as previously matched by a capturing group.
Example: 
/([dbc])([de])\2\1/g
1st Capturing Group 
([dbc])
Match a single character present in the list below 
[dbc]
dbc
matches a single character in the list dbc (case sensitive)
2nd Capturing Group 
([de])
Match a single character present in the list below 
[de]
de
matches a single character in the list de (case sensitive)
\2 matches the same text as most recently matched by the 2nd capturing group
\1 matches the same text as most recently matched by the 1st capturing group.


### Look-ahead and Look-behind
they are zero-length assertions just like the start and end of line, and start and end of word anchors explained earlier in this tutorial. The difference is that lookaround actually matches characters, but then gives up the match, returning only the result: match or no match. 
Example:

## Author

Contact me at https://github.com/mamadou1991.
