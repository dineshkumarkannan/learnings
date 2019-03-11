---
title:  "String - slice(), substring(), substr()"
date:   2019-03-08 15:12:00 +0530
categories: js
---

## String - slice() v substring():

 - char at &lt;end&gt; will not be displayed
 - &lt;end&gt; is optional

| | slice(start, end)	| substring(start, end) |
|:---|:---:|:---:|
| start == end | empty string | |
| end is omitted | extracts characters to the end of the string | |
| start / end > string.length | string's length will be used instead | |
| start > end | empty string | swaps two arguments |
| start = -ve | sets char from the end of string | treated as if it were 0 |
| end = -ve | Math.max(0, string.length + end) | |
| start / end = NaN | treated as if it were 0 | |

## String - substr():

| | substr(start, length) |
|:---|:---:|
| length - omitted / > string.length | extracts characters to the end of the string |
| start > string.length | empty string |
| start / length = -ve | empty string |
| start = NaN | treated as if it were 0 |
| length = NaN | empty string |
