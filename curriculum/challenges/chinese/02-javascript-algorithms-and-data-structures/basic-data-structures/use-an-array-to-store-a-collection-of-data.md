---
id: 587d7b7e367417b2b2512b20
title: 使用数组存储数据集合
challengeType: 1
forumTopicId: 301167
---

# --description--

以下是<dfn>数组（Array）</dfn>数据结构的最简单的实现例子。这是一个<dfn>一维数组（one-dimensional array）</dfn>，它只有一层，或者说在它里面没有包含其它的数组结构。可以看到它里面包含了<dfn>布尔值（booleans）</dfn>、<dfn>字符串（strings）</dfn>、<dfn>数字（numbers）</dfn>以及一些其他的 JavaScript 语言中合法的数据类型：

```js
let simpleArray = ['one', 2, 'three', true, false, undefined, null];
console.log(simpleArray.length);
// logs 7
```

可以在上述例子中看到，所有数组都有一个<dfn>长度（length）</dfn>属性。可以简单地使用`Array.length`方法来访问它。 下面是一个关于数组的更复杂的例子。这是一个<dfn>多维数组（multi-dimensional Array</dfn>），或者说是一个包含了其他数组的数组。可以注意到，在它的内部还包含了 JavaScript 中的<dfn>对象（objects）</dfn>结构。我们会在后面的小节中讨论该数据结构，但现在你只需要知道数组能够存储复杂的对象类型数据。

```js
let complexArray = [
  [
    {
      one: 1,
      two: 2
    },
    {
      three: 3,
      four: 4
    }
  ],
  [
    {
      a: "a",
      b: "b"
    },
    {
      c: "c",
      d: "d"
    }
  ]
];
```

# --instructions--

我们已经定义了一个名为`yourArray`的变量。请修改题目中的语句，将一个含有至少 5 个元素的数组赋值给`yourArray`变量。你的数组应该包含至少一个 <dfn>string</dfn> 类型的数据、一个 <dfn>number</dfn> 类型的数据和一个 <dfn>boolean</dfn> 类型的数据。

# --hints--

yourArray 应该是一个数组。

```js
assert.strictEqual(Array.isArray(yourArray), true);
```

`yourArray`至少要包含 5 个元素。

```js
assert.isAtLeast(yourArray.length, 5);
```

`yourArray`应该包含至少一个`boolean`。

```js
assert(yourArray.filter((el) => typeof el === 'boolean').length >= 1);
```

`yourArray`应该包含至少一个`number`。

```js
assert(yourArray.filter((el) => typeof el === 'number').length >= 1);
```

`yourArray`应该包含至少一个`string`。

```js
assert(yourArray.filter((el) => typeof el === 'string').length >= 1);
```

# --solutions--

