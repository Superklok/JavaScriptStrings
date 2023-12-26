# JavaScript Detect Capital
<br/>

## Challenge
Usage of capitals in a word will be deemed correct when one of the following cases is met:
- All letters in the word are capitals, like `'SUPERKLOK'` for instance.
- All letters in the word are not capitals, such as `'superklok'`.
- Only the first letter in the word is capitalized, as in `'Superklok'`.

Given a string word, return `true` if the usage of capitals in it is correct.
<br/>
<br/>

### 1<sup>st</sup> Example

```JavaScript
Input: word = 'SUPERKLOK'
Output: true
```

### 2<sup>nd</sup> Example

```JavaScript
Input: word = 'SuPeRkLoK'
Output: false
```

<br/>

### Constraints

- `1 <= word.length <= 100`
- `word` consists of lowercase and/or uppercase English letters.

<br/>

## Solution

```JavaScript
const detectCapitalUse = function(word) {
    return (word === word.toUpperCase() ||
            word === word.toLowerCase() ||
            word === word[0].toUpperCase() + word.slice(1).toLowerCase());
};
```

<br/>

## Explanation

I've decided to use the OR operator to return a Boolean based on three different acceptable condition possibilities.
<br/>

The first condition will return `true` if the `word` is truly equal to the `word` with the `toUpperCase` method applied which transforms the string into all capital letters. This validates that the `word` is correctly written in all capitals.
<br/>

The second condition will return `true` if the `word` is truly equal to the `word` with the `toLowerCase` method applied which transforms the string into all lowercase letters. This validates that the `word` isn't using any capital letters and it's written entirely in lowercase.
<br/>

The final condition will return `true` if the letter at `index 0` of the `word` (the first letter of the string) is the same as the first letter of the `word` with the `toUpperCase` method applied, and that all the letters from `index 1` to the end of the `word` (the second letter and all letters that follow it) are equivalent to the letters of the `word` at those indexes but with the `toLowerCase` method applied. This validates that the `word` is only using a capitalized character as the first letter of the `word` and all the other letters that follow are written in lowercase.
<br/>

If none of the above three conditions are met, then the function returns `false` to indicate that the capitalized characters are not being used correctly in the test string.
<br/>
<br/>
<br/>
<br/>

### :next_track_button: [Next (Reverse Words in a String III)][Next]
<br/>

### :previous_track_button: [Previous (Reverse String)][Previous]
<br/>

### :play_or_pause_button: [More String Challenges][More]
<br/>

### :eject_button: [Return to Course Outline][Return]
<br/>

[Next]: https://github.com/Superklok/JavaScriptStrings/blob/main/JavaScriptReverseWordsInAStringIII.md
[Previous]: https://github.com/Superklok/JavaScriptStrings/blob/main/JavaScriptReverseString.md
[More]: https://github.com/Superklok/JavaScriptStrings
[Return]: https://github.com/Superklok/LearnJavaScript