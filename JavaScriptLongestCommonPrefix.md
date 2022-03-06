# JavaScript Longest Common Prefix

## Challenge:

Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string `""`.

### 1<sup>st</sup> Example:

`Input: strs = ["flower","flow","flight"]`
<br/>
`Output: "fl"`

### 2<sup>nd</sup> Example:

`Input: strs = ["dog","racecar","car"]`
<br/>
`Output: ""`
<br/>
`Explanation: There is no common prefix among the input strings.`

### Constraints:

`1 <= strs.length <= 200`
<br/>
`0 <= strs[i].length <= 200`
<br/>
`strs[i]` consists of only lower-case English letters.

## Solution:

`const longestCommonPrefix = (strs) => {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`let ans = '';`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`for (i in strs[0]) {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`if (!strs.every((el) => el[i] === strs[0][i])) {`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`break;`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`ans += strs[0][i];`
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`}`
<br/>
<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`return ans;`
<br/>
`};`
<br/>
<br/>