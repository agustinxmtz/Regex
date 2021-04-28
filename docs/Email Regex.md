# Email Address Regex

Simple tutorial to demostrate how an email address functions with regular expressions, and the different steps needed to validate information for a user. 

## Summary

In this tutorial we will see how an email can be broken down for validation purposes. 
The regular expression displayed bellow will help us separate the "username", @ symbol, and domain name. There are different sets of characters to help validate an email address. 

``` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Escaped Characters](#escaped-characters)


## Regex Components

### Anchors

How can we begin to disect how an email address will be verified? Most email addresses start with aplhanumeric characters or special character, knowing this we can begin to look at how regex interprets this. An anchor symbol "caret" ```(^)``` becomes the username for an email, while the dollar "sign" ```($)``` is used in the domain name. 

We will use this example for demonstration purposes ``` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ```

``` (^) ``` and ``` ^[a-z0-9_\.-]+ ``` begins to match letters a-z, num 0-9, underscore, periods, or hyphen.

``` ($) ```  and  ``` ([a-z\.]{2,6})$ ``` will match the end of the string with letters a-z, or a period. 


### Quantifiers

We now need to find out how many charaters will be used, and quantifiers are great for that. We will use the "plus" ``` (+) ``` and "curly brackets" ``` ({}) ``` this will help specify the minimum and maximum number of characters. 

``` (+) ``` and ``` [\da-z\.-]+ ``` will match one or more specified characters

``` ({}) ``` and ``` ([a-z\.]{2,6})$ ``` matches within two to six characters


### OR Operator

OR Operators allow for characters or set characters to be interchangable. "square brackets" ``` ([]) ``` are used for that purpose, the characters inside the brackets become interchangable.

``` ([]) ``` and ``` [a-z\.] ``` matches any character inside the brackets from a to z or a period.


### Character Classes

Characters that are going to be matched can use "digits" ``` (\d) ```.

``` [\d] ``` and ``` [\da-z\.-] ``` matches with digits, letters from a to z, underscore, hyphen or period. 


### Grouping and Capturing

A group of regex that will match your string can be identified within parenthesis ``` (()) ```. 

``` ([]+))@([]+) ``` and ``` ([a-z0-9_\.-]+)@([\da-z\.-]+) ``` encolses a  group of regex to be matched to. 


### Bracket Expressions

A set of characters that will be matched to your string, will be identified within square brackets ``` ([]) ```.

``` ([]+))@([]+) ``` and ``` ([a-z0-9_\.-]+)@([\da-z\.-]+) ``` encloses a set of characters to be matched with. 


### Escaped Characters 

Specify the literal value of a special character by adding a backslash ``` (\) ``` in front of the special character. 

``` ([\.]+))@([\.]+) ``` and ``` ([a-z0-9_\.-]+)@([\da-z\.-]+) ``` the escaped character is the period


## Author

** Agustin Martinez ** 

Full Stack Developer 

* GitHub: [agustinxmtz](https://github.com/agustinxmtz)
* LinkedIn: [Agustin Martinez](https://www.linkedin.com/in/agustin-martinez-6282aa1b3/)
* Email: agustinxmtz@gmail.com