# operation-regular-show
A tutorial on Regex for matching an Email 

## Summary

Regular Expressions, often referred to as REGEX, are encoded text strings with the purpose of matching patterns in other strings. An email REGEX allows you to validate the structure of an email address.  In this tutorial we will brake down the basic structure of an email REGEX. Email REGEX's have many special characters, and at first glance it may look like a bunch of nonsense. We will go through each character as well as define and explain what exactly those characters are doing. The example we will be using is this one: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`


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



### Character Classes


### Grouping and Capturing
As regex's grow more and more complex, one can define specific groups or captures of the regex. You can require different sections of the regex to fulfill different requirements by using grouping constructs. We do this by using the ( `()` ), a.k.a parenthesis. These sections in the regex are known as subexpressions. In our email regex we see multiple instances of subexpressions such as: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`. To break it down simply, there are three different subexpressions. 
* The first group: `([a-z0-9_\.-]+)` followed by an @ symbol
* The second group: `([\da-z\.-]+)` followed by an optional `\` or `.`
* The third group: `([a-z\.]{2,6})`

### Bracket Expressions
As mentioned earlier, the expressions `[]` represents a range of characters that you would like to match. In the bracket expressions we can include all the characters we want and don't want.
* Ex: `[act]`, we can look for a string that has `a` or `c` or `t` regardless of the string length. All of the following examples would match: `"aaaaaaaa"`, `"coward"`, `"treasure"`, `"cat"` and `"tac"`.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
