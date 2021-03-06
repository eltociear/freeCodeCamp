---
id: bad87fee1348bd9aedf08826
title: 使用顺时针方向指定元素的内边距
challengeType: 0
videoUrl: 'https://scrimba.com/c/cB7mBS9'
forumTopicId: 18346
---

# --description--

如果不想每次都要分别声明`padding-top`，`padding-right`，`padding-bottom`和`padding-left`属性，可以把它们汇总在`padding`属性里面声明，如下：

`padding: 10px 20px 10px 20px;`

这四个值按顺时针排序：上，右，下，左，并且设置的效果等同于特定声明每一个方向的`padding`。

# --instructions--

按照顺时针顺序，给".blue-box" class的上内边距以及左内边距设置为`40px`，右内边距和下内边距则设置为`20px`。

# --hints--

`blue-box` class 的上内边距应为`40px`。

```js
assert($('.blue-box').css('padding-top') === '40px');
```

`blue-box` class 的右内边距应为`20px`。

```js
assert($('.blue-box').css('padding-right') === '20px');
```

`blue-box` class 的下内边距应为`20px`。

```js
assert($('.blue-box').css('padding-bottom') === '20px');
```

`blue-box` class 的左内边距应为`40px`。

```js
assert($('.blue-box').css('padding-left') === '40px');
```

你应该按照顺时针排序，汇总声明的方式来设置`blue-box`的`padding`值。

```js
const removeCssComments = (str) => str.replace(/\/\*[\s\S]+?\*\//g, '');
assert(
  /\.blue-box\s*{[\s\S]*padding[\s]*:\s*\d+px\s+\d+px\s+\d+px\s+\d+px(;\s*[^}]+\s*}|;?\s*})/.test(
    removeCssComments($('style').text())
  )
);
```

# --solutions--

