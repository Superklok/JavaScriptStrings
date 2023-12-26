# JavaScript Reverse Words in a String III
<br/>

## Challenge
Given a string `s`, reverse the order of characters in each word within a sentence while still preserving whitespace and initial word order.
<br/>
<br/>

### 1<sup>st</sup> Example

```JavaScript
Input: s = 'Here's a string of words'
Output: 'sdrow fo gnirts a s'ereH'
```

### 2<sup>nd</sup> Example

```JavaScript
Input: s = 'Superklok Labs'
Output: 'sbaL kolkrepuS'
```

<br/>

### Constraints

- `1 <= s.length <= 5 * 10⁴`
- `s` contains printable ASCII characters.
- `s` does not contain any leading or trailing spaces.
- There is at least one word in `s`.
- All the words in `s` are separated by a single space.

<br/>

## Solution

```JavaScript
const reverseWords = (s) => {
    return s.split(' ').map((w) => w.split('').reverse().join('')).join(' ');
};
```

<br/>

## Explanation

I've written a function expression, using ES6 syntax, that is defined by an anonymous function that accepts `s` as a string of words.
<br/>

Within the anonymous function, the string `s` is split into an array of string words everywhere there is a space `' '` by using the string prototype `split` method.
<br/>

The array prototype `map` method is then applied to the array that was returned by the `split` method. The string words `w` in the array are then split into their own arrays of string characters using the string prototype `split` method at `''`.
<br/>

The string character arrays are then reversed using the array prototype `reverse` method. The newly reversed arrays are then joined together to form words `w` again, and this process is effectuated for each word from the array derived from `s`.
<br/>

Once the array prototype `map` method is complete, the reversed words are then joined into a string using the array prototype `join` method that adds a space `' '` between each reversed word.
<br/>
<br/>
<br/>
<br/>

### :next_track_button: [Next (Valid Palindrome)][Next]
<br/>

### :previous_track_button: [Previous (Detect Capital)][Previous]
<br/>

### :play_or_pause_button: [More String Challenges][More]
<br/>

### :eject_button: [Return to Course Outline][Return]
<br/>

[Next]: https://github.com/Superklok/JavaScriptStrings/blob/main/JavaScriptValidPalindrome.md
[Previous]: https://github.com/Superklok/JavaScriptStrings/blob/main/JavaScriptDetectCapital.md
[More]: https://github.com/Superklok/JavaScriptStrings
[Return]: https://github.com/Superklok/LearnJavaScript