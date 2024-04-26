---
layout: post
title: jekyll_页面
---
> {{page.title}}

### 添加页面的方法
- 在根目录中添加一个`.html`文件
- 编写一个`.md`文件并使用`front matter`块，会在构建时转换被为`.html`文件

### 组织在子目录中
- 默认生成在项目根目录
- 当在`front matter`块中设置不同的`permalink`值时，生成相应怒路