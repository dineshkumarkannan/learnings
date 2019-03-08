---
title:  "String - slice() v substring() v substr()"
date:   2019-03-08 15:12:00 +0530
categories: js
---

## String - slice() v substring() v substr():

- slice(start, end - optional)
  - char at &lt;end&gt; will not be displayed

- substring(start, end - optional)
  - char at &lt;end&gt; will not be displayed
  - if &lt;start&gt; &gt; &lt;end&gt;, it is interchanged

- substr(start, length)


string = '0123456789';

| start | end / length | slice(start, end) | substring(start, end) | substr(start, length) |
|:-----:|:------------:|:-----------------:|:---------------------:|:---------------------:|
|   1   |       3      |         12        |           12          |          123          |
|   7   |       3      |                   |          3456         |          789          |
|   3   |       3      |                   |                       |          345          |
|   -7  |      -3      |        3456       |                       |                       |
|   -3  |      -7      |                   |                       |                       |
|   3   |              |      3456789      |        3456789        |        3456789        |
|   -3  |              |        789        |       123456789       |          789          |
|   2   |      100     |      23456789     |        23456789       |        23456789       |
|  100  |      101     |                   |                       |                       |
|  NaN  |       8      |      1234567      |        1234567        |        1234567        |
|   1   |      NaN     |                   |           0           |                       |


## Valid / Invalid parameters:

|         |                   slice(start, end)                   |                          substring(start, end)                          |                substr(start, length)               |
|:-------:|:-----------------------------------------------------:|:-----------------------------------------------------------------------:|:--------------------------------------------------:|
|  Valid  | start < end / string.length start == NaN & end != NaN | start || end == -ve start == NaN & end != NaN start != NaN & end == NaN | start & length == -ve start == NaN & length != NaN |
| Invalid | start >= end / string.length  end == NaN              | start && end == -ve start == end start & end == NaN                     | start & end == -ve values length == NaN            |
