---
layout: default
title: 下拉菜单
level: 2
summary: 
guide: https://v2.bootcss.com/components.html#dropdowns
---
## {{page.title}}
- 声明类选择器`dropup``dropdown`
  - 相对定位，用于包裹绝对定位元素

```css
.dropup,
.dropdown {
  position: relative;
}
```
- 声明类选择器`dropdown-menu`
  - 绝对定位
  - 底部显示
  - 左对齐
  - 隐藏

```css
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  background-color: #ffffff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  *border-right-width: 2px;
  *border-bottom-width: 2px;
  -webkit-border-radius: 6px;
     -moz-border-radius: 6px;
          border-radius: 6px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
     -moz-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
          box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  -webkit-background-clip: padding-box;
     -moz-background-clip: padding;
          background-clip: padding-box;
}
```
- 声明且组合器`.dropdown-menu.pull-right`
  - 右对齐

```css
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
```