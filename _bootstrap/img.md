---
layout: default
title: 图片
summary: 
level: 1
guide: https://v2.bootcss.com/scaffolding.html#layouts
---

- 声明元素选择器，裁切圆角使用绝对值500，为什么不使用50%
- border-radius半径值超过一半时最大取一半值

```css
img {
  width: auto\9;
  height: auto;
  max-width: 100%;
  vertical-align: middle;
  border: 0;
  -ms-interpolation-mode: bicubic;
}
```
- 声明类选择器`img-circle`

```css
.img-rounded {
  -webkit-border-radius: 6px;
     -moz-border-radius: 6px;
          border-radius: 6px;
}

.img-polaroid {
  padding: 4px;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  -webkit-box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
     -moz-box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
          box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
}

.img-circle {
  -webkit-border-radius: 500px;
     -moz-border-radius: 500px;
          border-radius: 500px;
}
```