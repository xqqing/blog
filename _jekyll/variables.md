---
layout: default
title: 变量
summary:  页面中可以访问的变量
level: 1
guide: https://jekyllrb.com/docs/variables/
---
{{ page.name }}

Jekyll穿越`traverse`站点查找要处理的文件。  
任何带`front matter`文件被处理。  
为每个文件Jekyll通过`Liquid`提供了各种可用数据。


## 全局变量

| 变量名    | 描述                                 |
| --------- | ------------------------------------ |
| site      | 站点。在`_config.yml`设置            |
| page      | 页面。在`front matter`设置自定义变量 |
| layout    | 布局。                               |
| content   | 内容。在布局文件中，页面或文章的内容 |
| paginator | 分页。配置paginate选项时生效         |

### site变量的属性

| 变量名              | 描述                                                                    |
| ------------------- | ----------------------------------------------------------------------- |
| time                | 当前时间。执行Jekyll命令时                                              |
| pages               | 全部页面。                                                              |
| posts               | 全部文章。时间逆序列表                                                  |
| related_posts       | 相关文件。默认最近10篇文章                                              |
| static_files        | 全部静态文件。静态文件5个属性：path/modified_time/name/basename/extname |
| html_pages          | pages中.html结尾                                                        |
| html_files          | static_files中.html                                                     |
| collections         | 全部集合                                                                |
| data                | _data目录中加载.yml文件的数据                                           |
| documents           | 每个collection中全部文档                                                |
| categories.CATEGORY | CATEGORY类别中全部文章                                                  |
| tags.TAG            | TAG标签中全部文章                                                       |
| url                 | 网站url                                                                 |
| .[CONFIGURATION]    | 通过命令行或_config.yml设置的变量。可以省略.直接使用[]                  |

### page变量的属性

| 变量名     | 描述                                              |
| ---------- | ------------------------------------------------- |
| content    | 内容                                              |
| title      | 标题。                                            |
| excerpt    | 摘录。                                            |
| url        | 域名后面部分的URL。                               |
| date       | 文章日期，可以在开头指定。                        |
| id         | 文档唯一标识                                      |
| categories | 文章所属全部类别                                  |
| collection | 文档所属集合。                                    |
| tags       | 文章所属全部标签。                                |
| dir        | 所属路径，可以使用permalink指定。                 |
| name       | 名称。                                            |
| path       |
| next       | 下一个文章，在site.posts列表中，最后一个时返回nil |
| previous   | 前一个文章                                        |
| .CUSTOM    | 自定义属性                                        |
