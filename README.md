# Regex-tutorial
A tutorial for Regex

The use of this expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` can be used to match and validate emails for when you use technologies like Node(inquirer) and MongoDB

## Summary

This tutorial will go through the proccess of applying regex to match an email and talk about it's components. Some content that we will discuss pertaining to Regex are anchors, quantifiers, grouping constructs, bracket expressions, character classes, the OR operator, flags and character escapes. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors
The caret ^ and dollar $ characters have special meaning in a regexp. They are called “anchors”.
The caret ^ matches at the beginning of the text, and the dollar $ – at the end.
Anchors do not match any characters, they match a position before or after characters.

### Quantifiers

Regex Quantifiers includes the `+` operator, which will connect the users email name + email service + `.com`. Another quantifier includes `{2,6}`, which will allow a match range of 2-6 characters for the character set of `[a-z\.]`.

### Character Classes
The character class in this expression is `\d`, which matches a single characters that is a digit from 0-9. It will only match a single digit such as "4", but not "44". 

### Grouping and Capturing
Capturing group #1 in this expression is `([a-z0-9_\.-]+)` that matches the user email name. The second capturing group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})` to capture the `.com`.

### Bracket Expressions
Bracket expressions for email validation includes the character sets of `[a-z0-9_\.-]`, which is matching any letter a-z and is case sensitive. It also matches a character 0-9 and matches the characters "_" , "-" , and "."; `[\da-z\.-]`, which is matching a single digit from 0-9, any character a-z (case sensitive), and the characters "." and "-".; `[a-z\.]` matches any character a-z(case sensitive) and the character ".". 

### Greedy and Lazy Match
This regrex includes greedy matches. Since it includes the `+` Quantifier, it will match as many times as possible giving back as needed. Another greedy Quantifier used in this regex is `{}` when matching `{2,6} for the last capture group.
