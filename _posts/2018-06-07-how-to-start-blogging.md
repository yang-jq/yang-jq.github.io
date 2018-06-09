---
title: "10分钟构建博客"
layout: post
excerpt_separator: <!--more-->
category: [Github Pages, Jekyll]
tag: [Github Pages, Jekyll]
published: true
permalink: /how-to-start-blogging.html
---


[Jekyll](https://jekyllrb.com/)([中文](https://www.jekyll.com.cn/))是将Markdown等轻量化标记语言编写的文本转换为静态网页的工具，而[Github Pages](https://pages.github.com/)是Github提供的静态网页托管服务。既有生成工具，又有托管服务，两者结合就可以便捷地创建个人博客或项目主页。
<!--more-->

### 从模板开始
从零开始亲手创建精致的个人博客当然需要耗费不少精力和时间，但幸好已经有不少优秀的开源博客模板可供直接选用。此处列举了一些：

|模板名称|模板预览|
|:---:|:---:|
|[NexT](https://github.com/simpleyyt/jekyll-theme-next)([官网](http://theme-next.simpleyyt.com/))|[NexT预览]({{"/blog_images/start-your-blogging/NexT_preview.png" | absolute_url}})|
|[TeXt](https://github.com/kitian616/jekyll-TeXt-theme)|[TeXt预览]({{"/blog_images/start-your-blogging/TeXt_preview.png" | absolute_url}})|
|[Flexible](https://github.com/artemsheludko/flexible-jekyll)|[Flexible预览]({{"/blog_images/start-your-blogging/Flexible_preview.png" | absolute_url}})|
|[官方模板](https://pages.github.com/themes/)|[官方预览]({{"/blog_images/start-your-blogging/Official_preview.png" | absolute_url}})|
|[Jekyllthemes.org](http://jekyllthemes.org/)|[网站预览]({{"/blog_images/start-your-blogging/Jekyllthemes_org.png" | absolute_url}})|
|[Jekyll-themes.com](https://jekyll-themes.com/)|[网站预览]({{"/blog_images/start-your-blogging/Jekyll-themes_com.png" | absolute_url}})|

下面以NexT模板为例搭建博客。
- **Step 1**: 注册[Github](https://github.com/)账号，记Github用户名为`userid`。
- **Step 2**：将NexT模板仓库(Repository)Fork到你的Github空间，将刚Fork到的NexT仓库更名为：`userid.github.io` (`NexT仓库页面` &rarr; `Settings` &rarr; `Rename`)
- **Step 3**：你的博客已上线。在浏览器地址栏输入`https://userid.github.io`尝试访问吧。[[此处是本人博客]](https://yang-jq.github.io/)。

### 定制版面
你可能需要调整博客版面以符合你的审美。调整版面需要修改`_config.yml`文件，可以直接在博客仓库里在线修改。但在以后的博客写作中，通常是在本地完成撰写后，再通过Git命令或Github Desktop推送到Github，所以还是趁现在把需要用到的工具安装上吧。
- **Step 1**：安装[Github Desktop](https://desktop.github.com/)，并通过Github账户登录，将博客仓库下载到本地。
- **Step 2**：使用文本编辑器修改`_config.yml`全局配置文件，关于NexT主题的配置项可参考[NexT主页](http://theme-next.simpleyyt.com/)的说明：

|常用配置项|功能说明|可选值|示例|
|:---:|:---:|:---:|:---:|
|`title`|博客名称|字符串|`title: my blog`|
|`rss`|RSS订阅|`false`/留空/具体地址|`rss: false`，即不启用|
|`highlight_theme`|代码高亮样式|`normal`/`night`/`night eighties`/`night blue`/`night bright`|`highlight_theme: normal`|










### 版面定制
虽然你已经可以通过个人Github链接访问刚创建的博客，但版式还保留原样，还需要进一步对版式进行调整。这需要用到Github Desktop。

- **Step 1**：下载[Github Desktop](https://desktop.github.com/)，安装并通过Github账号登陆。
- **Step 2**：浏览器登陆Github，在个人博客仓库(`usedid/userid.github.io`)-->`Clone or download`，将博客仓库下载到本地。
- **Step 3**：打开本地仓库(默认路径为`/Documents/GitHub/userid.github.io`)，用文本编辑软件（如Notepad++）打开`_config.yml`，对当中的[全局配置项](http://theme-next.simpleyyt.com/theme-settings.html)进行设定：

|配置项|作用|可选值|示例|
|:----:|:---:|:---:|:---:|
|title|博客名称|任意字符串|`title: "my blog"`|
|rss|RSS订阅功能|`false`/留空/具体地址|`rss: false`|


### 新增博文
- *Step 1*：文件夹`_posts`为已经发布的博客，可以删除已有博客文档，并新建自己的博客文档。新建文档需要以`年-月-日-标题.后缀`命名，例如：`2018-06-07-How-to-write-blog.md`。

```
---
# 两个---之间的区域会被Jekyll当作YAML头信息进行处理，用于设置版面样式或设定某些变量，可以用#进行注释
title: "How to write blog"
layout: post # 可选值为：archive, category, index, layout, page, post, tag, 参见_layouts文件夹
date: 2018-06-09 20:40:00  # 缺省情况下，使用文档名中指定的日期
category: [Github, Jekyll]  # 也可以用categories: [xx, yy]
published: true  # 控制是否显示，缺省情况下为true，可设置为false
tags: [Github, Jekyll]
excerpt: "It is time to start your journal of blogging"  # 该篇文章的摘要
# excerpt_separator: <!--more-->  # 出现在excerpe_separator之前的文字作为摘要
---
以下是博客内容...
```
```python
import numpy as np
from matplotlib import pyplot as plt
def f(a, b):
    return a + b
```
