---
title:  "Data Types"
date:   2018-08-28 10:31:00 +0530
categories: js
---

- Number
  - Special numbers: Infinity, -Infinity, NaN
- String
- Boolean
  - true, false (0, NaN, "")
  - console.log(NaN == NaN);  //false
- Object
- Undefined


### Negative Infinity (-Infinity)
  Negative number divided by 0


### null v undefined

  || null | undefined |
  |---|---|---|
  | means | Assigned value, means nothing<br>needs explicit assignment | Variable declared, but not defined.<br>*Variable's default value.* |
  | typeof | object | undefined |

  ```js
  var a; //undefined
  var b = null; //null

  null = 'value' //Reference error
  undefined = 'value' //value
  ```

  ```js
  null == undefined  //true

  null === undefined  //false
  null == 0  //false
  ```

  ```js
  var undefined = null;
  undefined === null //true
  ```

### [Type coerecion equations](https://codeburst.io/javascript-why-does-3-true-4-and-7-other-tricky-equations-9dd13cb2a92a)

  Operator between number and boolean, or between booleans. boolean is converted to number (true == 1, false == 0).

  ```js
  3 + true  //4
  3 - true  //2
  3 * true  //3
  3 / true  //3

  3 + false //3
  3 - false //3
  3 * false //0
  3 / false //Infinity

  true + false  //1
  ```

  Add operator between string and number/boolean. number/boolean is converted to string.

  ```js
  'string' + 4  //string4

  'string' + true //stringtrue
  'string' + false //stringfalse

  4 + 'string'  //4string

  true + 'string' //truestring
  false + 'string' //falsestring


  'string' - 4  //NaN
  'string' * 4  //NaN
  'string' / 4  //NaN

  4 - 'string'  //NaN
  4 * 'string'  //NaN
  4 / 'string'  //NaN
  ```
