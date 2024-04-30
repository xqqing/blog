---
layout: default
title: CSS选择器
summary: 选择HTML元素
level: 1
guide: https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Selectors
---
## 选择器是什么
- 浏览器解析CSS选择器，选择指定HMTL元素，应用CSS规则中的样式

## 选择器列表
- 样式相同的多个选择器可以组合在一起，用逗号,分隔

## 选择器种类

| 种类                         | 语法     | 说明                         |
| ---------------------------- | -------- | ---------------------------- |
| 通配`universal`选择器        | *        |
| 元素`element`选择器          | a        |
| 类`class`选择器              | .link    |
| ID选择器                     | #mdn     |
| 属性`attribute`选择器        | [href]   | 类和ID选择器也属于属性选择器 |
| 伪类`pseudo-class`选择器     | a:hover  | 元素处于特定状态，附属选择器 |
| 伪元素`pseudo-element`选择器 | a::after | 元素中加入新元素，附属选择器 |

### 属性选择器


| 语法           | 说明                                      |
| -------------- | ----------------------------------------- |
| [name]         | 有属性name的元素                          |
| [name=value]   | 属性name的值等于value的元素               |
| [name~=value]  | 属性name的值空格列表出现value的元素       |
| [name\|=value] | 属性name的值等于value或以value-开始的元素 |
| [name^=value]  | 属性name的值以value开始的元素             |
| [name$=value]  | 属性name的值以value结束的元素             |
| [name*=value]  | 属性name的值字符串中出现value的元素       |

~=与*=的区别


## 关系选择器或组合器

| 种类     | 语法                    | 说明                                           |
| -------- | ----------------------- | ---------------------------------------------- |
| 后代     | 选1 (空格)选2。div span | 在满足选1的元素后代中满足选2的元素             |
| 子代     | 选1>(大于)选2。div>span | 在满足选1的元素子代中满足选2的元素             |
| 下个兄弟 | 选1+(加号)选2。div+span | 在满足选1的元素下个同代中满足选2的元素         |
| 后面兄弟 | 选1~(波浪)选2。div~span | 在满足选1的元素后面同代中满足选2的元素         |
| 且       | 选1选2。div.span        | 满足选1且满足选2。选1和选2不能同时为元素选择器 |
| 或       | 选1,(逗号)选2。div,span | 满足选1或满足选2。就是选择器列表               |

**无法选择父代或祖先**

