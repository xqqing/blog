---
layout: default
title: 网格系统
summary: 默认12列宽60间距11个宽20总宽940的容器
level: 1
guide: https://v2.bootcss.com/scaffolding.html#gridSystem
---

- 先使用元素选择器设置默认样式

## 网格系统
- 声明类选择器`.row`，和它的伪类选择器`.row::before/after`
- 左边距-20为了与内部首个`span*`左边距20抵消

```css
.row {
  margin-left: -20px;
  *zoom: 1;
}

.row:before,
.row:after {
  display: table;
  line-height: 0;
  content: "";
}

.row:after {
  clear: both;
}
```
- 声明属性选择器`[class*="span"]`，选择class属性的值为span开头的全部元素，设置`span*`浮动、左边距
- 声明类选择器`.span1-12`，设置`span*`宽度

```css
[class*="span"] {
  float: left;
  min-height: 1px;
  margin-left: 20px;
}
.span12 {
  width: 940px;
}

.span11 {
  width: 860px;
}

.span10 {
  width: 780px;
}

.span9 {
  width: 700px;
}

.span8 {
  width: 620px;
}

.span7 {
  width: 540px;
}

.span6 {
  width: 460px;
}

.span5 {
  width: 380px;
}

.span4 {
  width: 300px;
}

.span3 {
  width: 220px;
}

.span2 {
  width: 140px;
}

.span1 {
  width: 60px;
}
```
- 声明类选择器`.offset1-12`，跟在`span*`后可以重设左边距向右移动

```css
.offset12 {
  margin-left: 980px;
}

.offset11 {
  margin-left: 900px;
}

.offset10 {
  margin-left: 820px;
}

.offset9 {
  margin-left: 740px;
}

.offset8 {
  margin-left: 660px;
}

.offset7 {
  margin-left: 580px;
}

.offset6 {
  margin-left: 500px;
}

.offset5 {
  margin-left: 420px;
}

.offset4 {
  margin-left: 340px;
}

.offset3 {
  margin-left: 260px;
}

.offset2 {
  margin-left: 180px;
}

.offset1 {
  margin-left: 100px;
}
```
- 嵌套`row`和`span*`

```html
<div class="row">
  <div class="span2">
    <div class="row">
      <div class="span1"></div>
    </div>
  </div>
</div>
```
