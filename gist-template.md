# JavaScript Date Validator

This repository provides an overview and explanation of a regular expression (regex) in JavaScript that validates date strings in the "YYYY-MM-DD" format.

## Summary

This regex validates a date string to ensure it conforms to the "YYYY-MM-DD" format, with a four-digit year (between 1900 and 2099), a two-digit month (between 01 and 12), and a two-digit day (between 01 and 31).

Here's a breakdown:

    ^ asserts start of a line.
    (19|20) matches the strings "19" or "20" - these correspond to the first two digits of the year.
    \d\d matches any two digits - these correspond to the last two digits of the year.
    [-] is a literal match for the hyphen character.
    (0[1-9]|1[012]) matches a two-digit month: "01" to "09" or "10" to "12".
    [-] is another literal match for the hyphen character.
    (0[1-9]|[12][0-9]|3[01]) matches a two-digit day: "01" to "09", "10" to "29", or "30" to "31".
    $ asserts the end of the line.

This way, the regex makes sure the entire input is a date in the "YYYY-MM-DD" format.

## Code Snippet

let dateRegex = /^(19|20)\d\d[-](0[1-9]|1[012])[-](0[1-9]|[12][0-9]|3[01])$/;

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

Anchors are used to specify the position of the pattern in relation to a line of text. In our regex, ^ and $ are used as start and end line anchors respectively.

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. In our regex, \d\d and (0[1-9]|1[012]) use quantifiers to define the amount of digits required.

### Grouping Constructs

Grouping constructs ( ) are used to create subexpressions of the regex to be used by a quantifier, alternation, or for backreferencing. In our regex, (19|20) and (0[1-9]|[12][0-9]|3[01]) are used as grouping constructs.

### Bracket Expressions

Bracket expressions [] define a character class, a set of characters to match. In our regex, [1-9] is used within the grouping constructs to match a range of numbers.

### Character Classes

Character classes are a set of characters enclosed by a pair of square brackets []. The character class can match any single character contained in the set. In our regex, \d is a character class representing all digits.

### The OR Operator

The OR operator | allows the regex to match the pattern before or the pattern after the operator. In our regex, the OR operator is used in (19|20) to match "19" or "20" and in (0[1-9]|1[012]) to match "01" to "09" or "10" to "12".

### Flags

Flags are used to change how the regex pattern is interpreted. This regex does not use any flags, but commonly used ones include g for global search, i for case-insensitive search, and m for multiline search.

### Character Escapes

Character escapes are used to allow for special characters to be used as literal characters. This regex does not have any character escapes, but a commonly used one is \ to escape special characters.

## Author

My name is Matt Moore I am currently in a full-stack development profile and if you are interested here is a link to my github https://github.com/MattrMoore

