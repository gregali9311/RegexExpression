# Title (replace with your title)

Introductory paragraph (replace this with your text)



## Summary

In this tutorial, we will demonstrate how to use a Regular Expression (regex), specifically with a regex that identifys a matching email. 

The regex function that we will break down is as follows:

Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
Anchors don't match any specific character, but rather make an assumption about the characters being searched for. The anchor suggests that position matters- that is, it will search for characters at either the beginning or end of a string (for example).

In our matching email regex, the /^ indicates that this search is at the beginning of the string. 


### Quantifiers
In our regex expression, we have the following: 
### {2,6}
### 
Quantifiers are used to control how many times your regex matches to your search criteria. They are inherently greedy, meaning they will match as many iterations as possible unless specified otherwise. 
### 
In our example above, it is suggesting that we want to find the  pattern suggested in the regex at least 2 times, and not more than 6 times. 

### Grouping Constructs

Grouping constructs allows for checking multiple parts of a string. During our search using a regex, we may want to check different sections of the string based upon a given criteria. In our current expression: 
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Can se seen to have 3 different constructs:

#### ([a-z0-9_\.-]+)
#### ([\da-z\.-]+)
#### ([a-z\.]{2,6})

#
### Bracket Expressions
Inside of the constructs are the bracket expressions. Bracket expressions articulate the requirements for search- or better to say, they contain the expressions that articulate the search requirements. 

As seen below: 
#### [a-z0-9_\.-]
#### [\da-z\.-]
#### [a-z\.]
#

### Character Classes
Inside of our bracket expression are our character classes. In our expression, we have the following character classes:
#
### <b>a-z</b>
is a character class that searches for all characters that are lowercase between a-z, or any lower case character. Regexs are case sensitive. 
#### <b>0-9</b> 
indicates that any number between 0-9 can be used and is a character class.
#### _ 
indicates that the undescore can be used
#### \ 
is an escape character, that will be discussed in a later section. It allows for the "." to be interpreted literally, instead of as a character class

#### In our second bracket expression, we see <b>\d</b> character class, which acts synonymously to our 0-9 character class 

#
### The OR Operator
In our current regex, there is no OR Operator, but it would read as follows: 
#### 
(abc) --> (a|b|c), and be it would read that the search could find either abc or acb or cba. It makes the order irrelevant from the initial construct of (abc)
#
### Flags
#### 
Flags are additional ways to control the regex expression, but used at the end of the expression. The three most likely to be encountered 
### g- a global search
### i- case-insensitive search 
### m- multi line search s

#
### Character Escapes
When characters have classes, they will default to their character class. If the regex is to use the character literally, instead of as its character class, the "\" must precede the character class, and will subsquently be interpreted literally. 


## Author

My name is Greg Ali. I like long walks on the beach and boxing. Not usually at the same time. Here is my github link: 
https://github.com/gregali9311/
