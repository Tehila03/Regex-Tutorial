# Understanding the Email Validation Regex

## Introduction

Welcome to this JavaScript regex tutorial! Understanding regular expressions (regex) is essential for handling text patterns effectively. In this tutorial, we'll focus on a specific regex used for email validation. We'll break down each part, explain its purpose, and demonstrate how it ensures a valid email format. By the end, you'll have a solid understanding of this regex pattern and its practical application in web development projects.

## Summary

This is the regex code that we will be anaylizing today is: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;`

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

The anchors used to contain this regular expression are: `^` to start, and `$` to finish.

### Quantifiers

In this example, we used `+` to communicate there is another sequence to be matched as a greedy quantifier. We also used `{2,6}` as another greedy quantifer to specify the input should be a minimum of 2 characrtors to a maximum of 6 characters.

### OR Operator

An OR operator `(|)` means that the expression `[abc]` could be written as `(a|b|c)`.
In the example, email does not have an Operator included.

### Character Classes

In this regular expression, the charactor class `/d` is used which in Javasctipt classifies the use of any digit from 0 to 9.

### Flags

In JavaScript, you can add flags to a regex pattern to modify its behavior. We'll explore flags like `i` (case-insensitive), `g` (global), `m` (multiline), and `u`(unicode) and see how they affect the matching process.
In the example, there are no flags being used.

### Grouping and Capturing

Parentheses `()` are used for grouping in regex. They create capture groups that allow us to capture and extract specific parts of the matched text. In the given regex, there are three capture groups:

1. `([a-z0-9_\.-]+)`: Matches the local part of the email address (e.g., username).
2. `([\da-z\.-]+)`: Matches the domain name before the top-level domain (e.g., gmail).
3. `([a-z\.]{2,6})`: Matches the top-level domain (e.g., com, org).

### Bracket Expressions

Bracket expressions are anything inside a set of square brackets `([])`. These represent a range of characters that are meant to match.

In this example, there are 3 bracket expressions:

1. This represents the case sensitive characters from a-z, numbers from 0-9, an underscore, periods and hyphens.
   `[a-z0-9_\.-]`
2. This represents the all digits, case sensitive characters from a-z, periods and hyphens.
   `[\da-z\.-]`
3. This represents the case sensitive characters from a-z and periods.
   `[a-z\.]`

### Greedy and Lazy Match

In this example we have only used greedy quantifiers `+` and `{}`, meaning that it will allow the match to expand as long as it neess to go. If these quantifiers were lazy quantifiers, they would appear as `+?` or `{}?`, this will direct the system to make the shortest match.

### Boundaries

Boundaries in regex help us identify specific positions in the text. For example, we might want to match only the email address at the beginning of a sentence or a line. We'll see how to use boundaries to achieve this.
We do not use boundaries in this example.

### Back-references

Back-references allow us to match the same text that was previously matched by a capturing group. They are handy when we want to ensure that the same content repeats in the text.
Back-references are not used in this example.

### Look-ahead and Look-behind

Look-ahead is the syntax is: `X(?=Y)`, and it means that it will look for `X`, but match only if followed by `Y`.
Look-behind is similar, but it looks behind. That is, it allows to match a pattern only if there’s something before it.
These are not used in this example.

## Conclusion

Congratulations! You've successfully learned how to understand and interpret the email validation regex. Regular expressions are powerful tools for handling text patterns, and this example demonstrates their practical usage. Practice working with regular expressions to become proficient in using them effectively. Happy coding!

## Author

My name is Tehila Tal

Here is my GitHub repository: https://github.com/Tehila03
