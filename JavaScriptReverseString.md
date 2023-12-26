# JavaScript Reverse String
<br/>

## Challenge

Write a function that reverses a string. The input string is given as an array of characters `s`.

You must do this by modifying the input array in-place with `O(1)` extra memory.
<br/>
<br/>

### 1<sup>st</sup> Example

```JavaScript
Input: s = ['s','u','p','e','r','k','l','o','k']
Output: ['k','o','l','k','r','e','p','u','s']
```

### 2<sup>nd</sup> Example

```JavaScript
Input: s = ['R','a','c','e','c','a','r']
Output: ['r','a','c','e','c','a','R']
```

<br/>

### Constraints

- `1 <= s.length <= 10⁵`
- `s[i]` is a printable ascii character.

<br/>

## Solution

```JavaScript
const reverseString = (s) => {
    s.reverse();
};
```

<br/>

## Explanation

I've created a function expression, using ES6 syntax, that is defined by an anonymous function that accepts `s` as an array of string characters.
<br/>

Within the anonymous function, the `reverse` array prototype method is applied to the string array `s`. This will output the reverse of any array that the `reverseString` function is applied to.
<br/>
<br/>
<br/>
<br/>

### :next_track_button: [Next (Detect Capital)][Next]
<br/>

### :previous_track_button: [Previous (Code Smells)][Previous]
<br/>

### :play_or_pause_button: [More String Challenges][More]
<br/>

### :eject_button: [Return to Course Outline][Return]
<br/>

[Next]: https://github.com/Superklok/JavaScriptStrings/blob/main/JavaScriptDetectCapital.md
[Previous]: https://github.com/Superklok/ProgrammingPrinciples/blob/main/CodeSmells.md
[More]: https://github.com/Superklok/JavaScriptStrings/tree/main
[Return]: https://github.com/Superklok/LearnJavaScript