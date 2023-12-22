# JavaScript Longest Common Prefix
<br/>

## Challenge

Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string `""`.
<br/>
<br/>

### 1<sup>st</sup> Example

```JavaScript
Input: strs = ["flower","flow","flight"]
Output: "fl"
```

### 2<sup>nd</sup> Example

```JavaScript
Input: strs = ["dog","racecar","car"]
Output: ""
Explanation: There is no common prefix among the input strings.
```

<br/>

### Constraints

```JavaScript
1 <= strs.length <= 200
0 <= strs[i].length <= 200
```

- `strs[i]` consists of only lower-case English letters.

<br/>

## Solution

```JavaScript
const longestCommonPrefix = (strs) => {
    let ans = '';

    for (i in strs[0]) {
        if (!strs.every((el) => el[i] === strs[0][i])) {
            break;
        }

        ans += strs[0][i];
    }

    return ans;
};
```

<br/>

## Explanation

I've defined a function called `longestCommonPrefix` that takes an array of strings, `strs`, as input. The purpose of this function is to find the longest common prefix among all the strings in the array and return it as a single string.
<br/>

The function begins by initializing an empty string called `ans`, which will store the longest common prefix found so far.
<br/>

Next, the function enters a `for` loop that iterates over the characters of the first string in the input array, `strs[0]`.
<br/>

Inside the loop, there is an `if` statement that checks if every string in the input array has the same character at the current index, `i`, as the first string. This is done using the `every` array method and a callback function. If any string does not have the same character, the loop is exited using `break`.
<br/>

If all the strings have the same character at the current index, the character is appended to the `ans` string.
<br/>

After the loop finishes, the `ans` string now contains the longest common prefix among all the strings in the input array.
<br/>

Finally, the `ans` string is returned as the result of the function.
<br/>

In summary, this function iterates over the characters of the first string in the input array and checks if all the strings have the same character at each index. It builds the longest common prefix by appending the common characters to a result string. The resulting string is then returned as the output of the function.
<br/>
<br/>