# Regex-Tutorial

In this tutorial, we learn how to match a URL with regex. A regex is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

  ## Regex URL Example
```
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
```

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

Anchors control the start and end points in a search. The caret anchor, ```^```, matches the beginning of the string while the dollar anchor, ```$```, matches the end of the string. With ```^``` and ```$```, the string between them have to match.

In the "Regex URL Example" regex, the input string must start and end with something that conforms to the patterns defined between ```^``` and ```$``` like in the Regex URL Example.

### Quantifiers

Quantifiers determine how many instances of a token must be matched in the expression. The few quantifiers can be seen below.

- ```*``` - Matches the pattern zero or more times.
- ```+``` - Matches the pattern one or more times (not zero).
- ```?``` - Matches the pattern zero or one time.
- ```{}``` - Curly brackets can provide three different ways to set limits for a match:
  - ```{ n }``` - Matches the pattern exactly ```n``` number of times.
  - ```{ n, }``` - Matches the pattern pattern at least ```n``` number of times.
  - ```{ n, x }``` - Matches the pattern from a minimum of ```n``` number of times to a maximum of ```x``` number of times.

### OR Operator
The ```|``` acts like the boolean "or". Matches an expression before or after the ```|```. It works in a group or the entire expression and will be tested in order.

### Character Classes

Character classes define a set of characters that can occur within the string.
- ```[ABC]``` - used to match any character in brackets
- ```[^ABC]``` - used to match any character not in brackets
- ```[A-Z]``` - used to add dash between two characters in bracket range
- ```.``` - used to match any character except linebreaks
- ```[\s\S]``` - used to match any character including line breaks
- ```\w``` - used to match alphanumeric characters (0-9 or a-z or A-Z)
- ```\W``` - used to match any character not a word character
- ```\p```- used to match character in specified unicode category
- ```\d``` - used to match one decimal digit (0-9)

### Flags
Flags can change how the expression is interpreted. 
- ```i``` - ignores case
- ```g``` - global search retain index of last match made
- ```m``` - multiline flag makes the ```^``` and the ```$``` match start and end of line instead of string 
- ```u``` - Unicode
- ```y``` - only match lastIndex position
- ```s``` - ```.``` match any character

### Grouping and Capturing
A capture group does everything in the parentheses of a single unit. In the Regex URL Example above, there are 4 instances of capture groups in the expression:
- ```(https?:\/\/)```: Capture the protocol of the URL
- ```([\da-z\.-]+)```: Capture the domain of the URL
- ``` ([a-z\.]{2,6})```: Capture the top-level domain of the URL
- ```([\/w \.-]*)```: Capture any file paths or endpoints

### Bracket Expressions
Bracket expressions are represented in square brackets that match single character/element

### Greedy and Lazy Match
- Greedy - matches longest possible string, basically telling the engine to match as many instances of the token
- Lazy - matches shortest possible string, basically telling the engine to match the fewest amount of tokens

### Boundaries
```\b``` is an anchor similar to ```^``` and ```$```. It matches at a word bounday, which is zero length between two characters.

```\B``` matches at every position that ```\b``` does not. 

### Back-references
Back-references match the same text by capturing group. By putting the opening tag into a back-reference we cam reuse the name of the tag for the closing tag.

### Look-ahead and Look-behind
- ```(?=ABC)``` - positive look-ahead that matches a group after main expression 
- ```(?!ABC)``` - negative look-ahead that can not match a group after main expression
- ```(?<=ABC>)``` - positive look-behind that matches a group before the main expression
- ```(?<!ABC)``` - negative look-behind that can not match before the main expression

Look-aheads and look-behinds forces the main expressions to be what you defined it as.

## Author
Jongwon Lee: UCB Bootcamp student
https://github.com/JongwonLee123


