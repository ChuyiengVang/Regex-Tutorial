# Regex Tutorial

This tutorial will go through and breakdown the different components of a
Regular Expression.  A Regular Expression is a special string for describing
a search pattern.

## Summary

The Regular Expression we will be using in this tutorial will be one that is
used for matching emails.  There is no Regular Expression that will match 100%
of all emails but we can get close.

```
/^[A-Za-z0-9_!#$%&'*+\/=?`{}~^.-]+@[A-Za-z0-9.-]+$/gm
```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

```
/^[A-Za-z0-9_!#$%&'*+\/=?`{}~^.-]+@[A-Za-z0-9.-]+$/gm
```

### Anchors

The Anchors in this Regex are " ```^```"  and "```$```". Anchors are what 
starts and ends a Regex.  The starting anchor "```^```" matches the beginning 
of the string and the ending anchor "```$```" matches the end of the string.  

### Quantifiers

The Quantifier "```+```" declares the data as part of our pattern.  For our example, 

```
[A-Za-z0-9_!#$%&'*+\/=?`{}~^.-]+
```

this will mean the string must conatins atleast one letter from A-Z/a-z or 
numbers from 0-9 or a special character that consists of _!#$%&'*+\/=?`{}~^.-.

### Grouping Constructs

In this tutorial we don't use Grouping Constructs.  In a Regex that would use 
one, there is capturing and non capturing.   Capturing groups in this example,

```
(ABCD)
```

"```()```" is used to capture "```ABCD```" and remember/stores the matched group.

```
(?:ABCD)
```

The "```?:```" syntax denotes a non capturing group and does not remember/store the 
match.

### Bracket Expressions

Bracket expressions are a list of characters/character classes wrapped with square
brackets "```[]```" which can be used to match a single character.  For our example, 

```
[A-Za-z0-9.-]+
```

this will match any charcter in range of characters A-Z, a-z, 0-9 which is seperated 
by a "```-```" or matches any character in the square brackets "```.-```".

### Character Classes

Character class are the set of characters enclosed within the square brackets.  In 
our example,

```
[A-Za-z0-9.-]+
```

"```A-Z```", "```a-z```" and "```0-9```" are defined as a character range, which is 
a type of character set which uses a "```-```" between the characters to imply the
entire range of characters between them which also includes the starting and ending 
characters.  "```.-```" are defined as character set, a set list of characters that 
may be a match in the search.

### The OR Operator

In this tutorial we don't use th "```|```" OR opertor but in this example, 

```
([ABCD]|[WXYZ])
```

Depending on how the match starts, it will return one or the other.

### Flags

Regex flags is a parameter that modifies its searching behavior.  For our example,

```
$/gm
```

"```g```" indicates that the search will be performed Globally and searches for all 
occurences and "```m```" is used to modify the behavior of "```^```" and "```$```", 
without "```m```" they match the start and end of the string only but in this case they
match start and end of each line within the string.

### Character Escapes

In this tutorial we don't use Character Escape.  "```\```" syntax is used when using character escape.  It's used to match special characters within the regex and is taken away in that one place.


## Author

You may contact me with any questions at:

Email: chuyieng@gmail.com
Github: github.com/ChuyiengVang
