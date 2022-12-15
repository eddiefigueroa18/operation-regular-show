# operation-regular-show
A tutorial on Regex for matching on Email 

## Summary

Regular Expressions, often referred to as REGEX, are encoded text strings with the purpose of matching patterns in other strings. An email REGEX allows you to validate the structure of an email address.  In this tutorial we will brake down the basic structure of an email REGEX. Email REGEX's have many special characters, and at first glance it may look like a bunch of nonsense. We will go through each character as well as define and explain what exactly those characters are doing. The example we will be using is this one: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

<!-- Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. -->

## Table of Contents
- [Regex Components](#regex-components)
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
There are many components to a REGEX and they are considered a literal. Because of this, we use characters to define what is a literal and what isn't by using the character ( `/` ),  a.k.a backslash. 
Example: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` Everything within the ( `/` ) is considered a literal. We will explain a little bit more in the anchors section below.

`///////////////////////////////////   break down regex here   \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\`

### Anchors
There are several types of anchors. For our email REGEX we we will be using ( `^` ) and ( `$` ). The ( `^` ) anchor represents a string that begins with the characters that follows it. This can go one of two ways. First, an exact string match. Second, a range of possible matches. 
* For an EXACT string match, Ex: `^Paper`, where the strings `"Paper"` or `"Paper airplanes"` will match. On the other hand `"paper"` and `"paper airplanes"` do not match with the anchors. As we mentioned before, this is because REGEX is case sensitive. Therefore anything within the ( `/` ) is literal, unless specified. 
* A RANGE of possible matches. This is done by using bracket expressions `[]`. Where anything inside the brackets symbolizes a range of characters that you want to match.

The ( `$` ) anchor represents a string that ends with the characters that precede the anchor. Much like the ( `^` ) anchor, it can use an exact string match or range of character matches. In our firs section of the email REGEX, the string must begin and end with anything that matches the pattern `[a-z0-9_\.-]`

### Quantifiers
* ( `+` ) This symbol matches the pattern one or more times.
    - In our email REGEX the `([\da-z\.-]+)` group, means the pattern within the group can be repeated more than once 

* ( `{}` ) These curly brackets limit character matches.
    - In our REGEX we can se that there is `{2, 6}` character limit. This means that we have want to search for the preceding string pattern a minimum of 2 times and a maximum of 6 times. 


### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
