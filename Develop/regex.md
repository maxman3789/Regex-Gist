# Let's Learn REGEX

A tutorial on the fundamentals of Regular Expressions (REGEX)

## Summary

A Regular Expression, or REGEX, is a sequence of characters that specifies a Search Pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.
For example, the following regular expression can be used to verify that user input is a valid email address:
> /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Regular expressions are used in search engines, search and replace dialogs of word processors and text editors

(https://en.wikipedia.org/wiki/Regular_expression)

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

### Anchors
Anchors assert that the engine's current position in the string matches a well-determined location: for instance, the beginning of the string, or the end of a line. 

The caret ^ matches the position before the first character in the string. Applying ^a to abc matches a. ^b does not match abc at all, because the b cannot be matched right after the start of the string, matched by ^.

Similarly, $ matches right after the last character in the string. c$ matches c in abc, while a$ does not match at all.

(https://www.rexegg.com/regex-anchors.html)
(https://www.regular-expressions.info/anchors.html)

### Quantifiers
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found.

> '*'	Match zero or more times.
> 
> '+'	Match one or more times.
> 
> '?'	Match zero or one time.
> 
> '{ n }'	Match exactly n times.
> 
> '{ n ,}'	Match at least n times.
> 
> '{ n , m }'	Match from n to m times.

(https://docs.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions)
(https://www.javascripttutorial.net/regular-expression-quantifiers/)

### Grouping Constructs
Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following:
* (expr) - Match or capture group. Captures the information that matches the expression in parentheses

* (?:expr) - Non-capturing group. Groups the contained expressions together (e.g., to apply a quantifier to multiple symbols at once), but does not restrict the information to be captured to only that group.

* (?=expr) - Captures information that is followed by the expression if the expression is true and the input matches the pattern that follows this expression.

* (?<>) - Named capture group.*

* \k<> - Named back reference. *

(https://docs.microsoft.com/en-us/dotnet/standard/base-types/grouping-constructs-in-regular-expressions)
(https://doc.laserfiche.com/laserfiche.documentation/en-us/Subsystems/ProcessAutomation/Content/Resources/Regular%20Expressions/Regular-Expression-Characters/Grouping-Constructs.htm)

### Bracket Expressions
A bracket expression is a list of characters enclosed by ‘[’ and ‘]’. It matches any single character in that list. If the first character of the list is the caret ‘^’, then it matches any character not in the list, and it is unspecified whether it matches an encoding error. For example, the regular expression ‘[0123456789]’ matches any single digit, whereas ‘[^()]’ matches any single character that is not an opening or closing parenthesis, and might or might not match an encoding error.

'elephant'.match(/[abcd]/) // -> matches 'a'

(https://www.gnu.org/software/grep/manual/html_node/Character-Classes-and-Bracket-Expressions.html)
(https://javascript.plainenglish.io/regular-expressions-brackets-f2d6f69ffe13)

### Character Classes
Character classes distinguish kinds of characters such as, for example, distinguishing between letters and digits.
[abc] matches a, b or c

(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Character_Classes)
(https://www.regular-expressions.info/refcharclass.html)

### The OR Operator
An example of the OR (||) Operator

> ^I like (dogs||penguins), but not (lions||tigers).$

The Result

>I like dogs, but not lions.
>
>I like dogs, but not tigers.
>
>I like penguins, but not lions.
>
>I like penguins, but not tigers.

(https://www.ocpsoft.org/tutorials/regular-expressions/or-in-regex/)

### Flags
Regular expressions have optional flags that allow for functionality like global searching and case-insensitive searching. These flags can be used separately or together in any order, and are included as part of the regular expression.

>const re = new RegExp('pattern', 'flags');

(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)

### Character Escapes
A character that otherwise would be interpreted as an unescaped language construct should be interpreted literally. For example, a brace ({) begins the definition of a quantifier, but a backslash followed by a brace (\{) indicates that the regular expression engine should match the brace. Similarly, a single backslash marks the beginning of an escaped language construct, but two backslashes (\\) indicate that the regular expression engine should match the backslash.

To match a character having special meaning in regex, you need to use a escape sequence prefix with a backslash (\). E.g., \. matches "."; regex \+ matches "+"; and regex \( matches "(".

(https://docs.microsoft.com/en-us/dotnet/standard/base-types/character-escapes-in-regular-expressions)
(https://www3.ntu.edu.sg/home/ehchua/programming/howto/Regexe.html)

## Author

This tutorial brought to you by Max S. (https://github.com/maxman3789)
