# Regex Tutorial: Matching a hexadecimal value

Regular expressions are a series of special characters that define a search pattern. There are methods to find exact values that match what we may be searching for, but if we need our search to be more encompassing. Imagine we have multiple different phone numbers and wanted to recieve all of them for a search. Instead of making an infinite amount of if statements to cover all cases we can use a regular expression to simply find cases of 9 numbers in a pattern of a phone number.
## Summary

A hex value is a value that can contain 0-9 and a-f in a regular expression it would look like:
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
We are gonna do a walkthrough of the components of a regular expression using this as an example.

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
Looking at the regex:
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The 2 slashes(/) are there to wrap the expression because it is considered a lateral and must be wrapped in slashes.
### Anchors
The characters `^` and `$` are considered anchor characters because they 'anchor' our expression. `^` signifies a string that follows it and `$` signifies a string that ends with the character that precedes it.
### Quantifiers
Quantifiers set the limits of the string that the regex matches. Frequently include minimum and maximum character length. The quantifiers in our expression are the `# `,`?`,and `{}`
`{}`- These represent the character length in our expression it means our expression can be exactly 6 or 3 characters.
`?`- this is saying after the ? it will be 0 or 1 characeters.

### OR Operator
`|` is the or operator in an expression it acts just as the english word or. In our expression:
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
The or is used so it searches for either of the paramaters set.

### Character Classes
A character class in a regex defines a set of characters. Some examples are `.`,`\d`,`\w`. etc.. Our expression does not contain any character classes.
### Flags
Flags are used for advanced searching in our expression. Our`^` and `$` in addition to anchoring our expression also allow expression to go across multiple lines of code.
### Grouping and Capturing
In a regex we use parentheses `()` to group parts of the expression into what we call subexpressions. In our expression:
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

We only have 1 sub expression. Grouping constructs have 2 categories, capturing and non-capturing. Capturing groups capture the matched character sequences for possible re use while non capturing does not.
### Bracket Expressions
`[]` represent a bracket expression which is used to represent a range of characters we want to match. In our expression
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`
This means it is searching for characters a-f or 0-9 of length 6 or characters a-f or 0-9 of lenngth 3. A note to remember the search is case sensitive if we wanted to include uppercase it would look like this:
`/^#?([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/`
### Greedy and Lazy Match
A Greedy match means it matches as many occurences of particular patterns as possible. 
A lazy match means it will match as few occurences as possible, a quantifier can be made lazy by adding the `?` symbol after it.    

### Boundaries
The concept of a boundary is similar to how we think of anchors `^` and `$` are technically boundaries another boundary is the `\b` known as the word boundary. This matches the whole word using a regex using `\b word \b`
### Back-references
In a capturing group we can use the contents in the string itself using back refrencing. it is used using `\N` where N is the group number.
### Look-ahead and Look-behind
A look ahead assertion  is used if you want to search for a string only if it is followed by another string `x(?=y)` matches x only if followed by y.

A look behind assertion is used if you want to search for a string only if it is preceeded by another string `(?<=y)x` matches x only if  x is preceeded by y.
## Author
[Github:Junya_jp](https://github.com/Junya-jp?tab=repositories)
[Email:junior_poku@hotmail.com](mailto:junior_poku@hotmail.com)

