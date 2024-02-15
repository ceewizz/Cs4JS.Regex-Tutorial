# Regex Tutorial


## Summary
For this Tutorial I will be covering the Hex Value /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
Expressions are used to generate characters combo to match a patern or string. For regular expressions or regex for short are a series of special characters that defines a search pattern.


## Table of Contents
<li><a href="#Anchors">[Anchors]</a></li>
<li><a href="#Quantifiers">[Quantifiers]</a></li>
<li><a href="Regex-Components">[Regex Components]</a></li>
<li><a href="#Or-operator">[OR-Operator]</a></li>
<li><a href="#Character-Classes">[Characters Classes]</a></li>
<li><a href="#Bracket-expressions">[Brackets Expressions]</a></li>


##  Regex Components
A regex is considered a literal, so the pattern must be wrapped in slash characters (/). If we examine the “Matching a Hex Value” regex, you'll see that this is true:
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/



### Anchors
The characters ^ and $ are both considered to be anchors.

The ^ anchor signifies a string that begins with the characters that follow it. This could be in one of two formats:
An exact string match, such as ^The, where the strings "The" or "The person" match, but "the" and "the person" do not. This is because a regex is case-sensitive.
A range of possible matches, displayed using bracket expressions. We'll discuss this in the next section.

So in our “Matching a Hex Value” regex, the string must start and end with something that matches the pattern

The $ anchor signifies a string that ends with the characters that precede it. Just as with the ^ character, it can be preceded by an exact string or a range of possible matches.
For Example:
f$ matches f in def while e$ doesn't match anything.
### Quantifiers
"/^#?([a-f0-9]{6}|[a-f0-9]{3})$/"
Set the limits of the string that your regex matches (or an individual section of the string). Quantifiers are inherently greedy, meaning they match as many occurrences of particular patterns as possible. They include the following:
*—Matches the pattern zero or more times

+—Matches the pattern one or more times

?—Matches the pattern zero or one time

{}—Curly brackets can provide three different ways to set limits for a match:

{ n }—Matches the pattern exactly n number of times

{ n, }—Matches the pattern at least n number of times

{ n, x }—Matches the pattern from a minimum of n number of times to a maximum of x number of times

Each of these quantifiers can be made lazy by adding the ? symbol after it, meaning it will match as few occurrences as possible.
So "/^#?([a-f0-9]{6}|[a-f0-9]{3})$/" the first "([a-f0-9]{6}" component will be 6 characters and the last component "|[a-f0-9]{3})$/" will match the length of 3 characters.


### OR Operator
 Often, you'll want to add this same logic outside of a bracket expression, especially within a grouping construct or between two different grouping constructs. Using the OR operator | element means it could be either of the components that we use an "|" to separate it with. In our original "/^#?([a-f0-9]{6}|[a-f0-9]{3})$/" means we will have 2 separate components


### Character Classes
A character class in a regex defines a set of characters, any one of which can occur in an input string to fulfill a match. We've actually already discussed some character classes. The bracket expressions outlined previously, including positive and negative character groups, are considered character classes.




### Bracket Expressions 
Matches any characters in the brackets are anything inside a set of square brakcets ([]) represents a range of characters that we want to match. So in our Matching a Hex value "/^#?([a-f0-9]{6}|[a-f0-9]{3})$/" We have 2 separate components searching for lowercase a-f and numbers 0-9.

