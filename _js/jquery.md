---
layout: collections
title: jQuery
level: 1
summary: JavaScript Library v1.12.4
---
## {{page.title}}`{{page.summary}}`
- 一个`IIFE`立即执行函数表达式`(function (global, factory){})()`
- 形参`global`:一个对象，实参`typeof window !== "undefined" ? window : this`。判断window是否未定义，已定义传window未定义传this。浏览器环境下window等于this
- 形参`factory`:一个函数，实参`function (window, noGlobal){}`。

```js
(function (global, factory) {/**/
}(typeof window !== "undefined" ? window : this, function (window, noGlobal) {/**/})
);
```

- 判断是否定义module对象，调用参数factor(是个函数)传入不同参数
- nodejs运行环境中会定义进入if语句
- 浏览器运行环境中不定义进入else语句，实参`factory(global, undefined)`

```js
function (global, factory) {
  if (typeof module === "object" && typeof module.exports === "object") {
    module.exports = global.document ?
      factory(global, true) :
      function (w) {
        if (!w.document) {
          throw new Error("jQuery requires a window with a document");
        }
        return factory(w);
      };
  } else {
    factory(global);
  }
}
```
- 真正实现功能的函数
- 参数`noGlobal`用于控制是否给参数`window`添加属性`jQuery`和`$`
- `jQuery === $`验证结果为true

```js
function (window, noGlobal) {
  /**/
  if (!noGlobal) {
    window.jQuery = window.$ = jQuery;
  }
  /**/
}
```