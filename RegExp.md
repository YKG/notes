# 正则

[TOC]

## 有用的网站
[Online regex tester and debugger: JavaScript, Python, PHP, and PCRE][6]

## 零宽度断言
### 一些例子：
- [匹配不包含"abc"的行(这个回答的解释部分很好)][1]
```
^((?!abc).)*$
```
- [其他][2]


## RegExp.lastIndex
```
r = /a/g;
s = 'a';
r.test(s); // true
r.test(s); // false  # 如果r没有用g修饰，这里的结果是true
```
[解释][3]


## Catastrophic Backtracking
大意是因为嵌套量词的使用，导致从出现大量的回溯，随着匹配字符串的增长，复杂度呈指数级上升。
一个例子：
```
r = /(0*)*A/;
s = "00000000000000000000000";
r.test(s);
```
上面的例子分别在三个浏览器下测试，结果如下：
浏览器      | 结果
------------|---------------
Chrome 35   | 无结果，无响应
IE 11       | 无结果，无响应
Firefox 30  | **flase**

Firefox在这个问题上的处理应该不正确。好像是它执行超过某个时间后就会返回false，实际上它并没有算出来结果。

### 参考
[Runaway Regular Expressions: Catastrophic Backtracking][4]
[如何中断正则的执行][5]


[1]: http://stackoverflow.com/questions/406230/regular-expression-to-match-string-not-containing-a-word
[2]: http://i.linuxtoy.org/docs/guide/ch26s09.html
[3]: http://www.cnblogs.com/52cik/p/js-regexp-test.html
[4]: http://www.regular-expressions.info/catastrophic.html
[5]: http://it.deepinmind.com/java/2014/06/17/how-to-interrupt-a-long-running-infinite-java-regular-expression.html
[6]: http://regex101.com/