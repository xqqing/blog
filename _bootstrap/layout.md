---
layout: default
title: 布局
summary: 
level: 1
guide: https://v2.bootcss.com/scaffolding.html#layouts
---

### 固定布局
- 声明类选择器`container`，设置宽度水平居中

```css
.container,
.navbar-static-top .container,
.navbar-fixed-top .container,
.navbar-fixed-bottom .container {
  width: 940px;
}
.container {
  margin-right: auto;
  margin-left: auto;
  *zoom: 1;
}

.container:before,
.container:after {
  display: table;
  line-height: 0;
  content: "";
}

.container:after {
  clear: both;
}
```
### 流式布局
- 声明类选择器`container-fluid`，设置水平内边距

```css
.container-fluid {
  padding-right: 20px;
  padding-left: 20px;
  *zoom: 1;
}

.container-fluid:before,
.container-fluid:after {
  display: table;
  line-height: 0;
  content: "";
}

.container-fluid:after {
  clear: both;
}
```
