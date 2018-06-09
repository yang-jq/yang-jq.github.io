---
title: "10分钟构建博客"
layout: post
excerpt_separator: <!--more-->
category: [Github Pages, Jekyll]
tag: [Github Pages, Jekyll]
published: true
permalink: /how-to-start-blogging.html
---


[Jekyll](https://jekyllrb.com/)([中文网](https://www.jekyll.com.cn/))是将Markdown等轻量化标记语言编写的文本转换为静态网页的工具，而[Github Pages](https://pages.github.com/)是Github提供的静态网页托管服务。既有生成工具，也有托管服务，两者结合就可以便捷地创建个人博客或项目主页。
<!--more-->

### 从模板开始
从零开始亲手创建精致的个人博客当然需要耗费不少精力和时间，但幸好已经有不少优秀的开源博客模板可供直接选用。此处列举了一些：

|模板名称|模板预览|
|:---:|:---:|
|[NexT](https://github.com/simpleyyt/jekyll-theme-next)([官网](http://theme-next.simpleyyt.com/))|[NexT预览]({{"/blog_images/start-your-blogging/NexT_preview.png" | absolute_url}})|
|[TeXt](https://github.com/kitian616/jekyll-TeXt-theme)|[TeXt预览]({{"/blog_images/start-your-blogging/TeXt_preview.png" | absolute_url}})|
|[Flexible](https://github.com/artemsheludko/flexible-jekyll)|[]({{"/blog_images/start-your-blogging/Flexible_preview.png" | absolute_url}})|
|[官方模板](https://pages.github.com/themes/)|[官方预览]({{"/blog_images/start-your-blogging/Official_preview.png" | absolute_url}})|
|模板网站|[Jekyllthemes.org](http://jekyllthemes.org/)|
|模板网站|[Jekyll-themes.com](https://jekyll-themes.com/)|

![NexT preview]({{"/blog_images/start-your-blogging/NexT_preview.png" | absolute_url}})


- **Step 1**：在[Github](https://github.com/)上注册账号。
- **Step 2**：挑选博客模板(又称为Theme或Template)：在[Jekyllthemes.org](http://jekyllthemes.org/)或[Jekyll-themes.com](https://jekyll-themes.com/)上选择一个你喜爱的模板；进入它的Github页面，然后将它Fork到你的Github上。这里有几个不错的Theme。下面以NexT主题为例进行讲解，Fork NexT主题后，它在仓库中的名称为`userid/jekyll-theme-next`，`userid`表示你的Github用户名)


![jpg absolute](http://ww1.sinaimg.cn/large/81b78497jw1emfgts2pt4j21hc0u0k1c.jpg)

jpg图片链接：{{"/blog_images/NexT_preview.jpg" | absolute_url}}

![jpg图片]({{"/blog_images/NexT_preview.jpg" | absolute_url}})

![jpg仓库地址](https://github.com/yang-jq/yang-jq.github.io/tree/master/blog_images/NexT_preview.jpg)

pdf绝对地址：{{"/pdfs/paper.pdf" | absolute_url}}

[pdf命令地址]({{"/pdfs/paper.pdf" | absolute_url}})

[_pdf命令地址]({{"/_pdfs/paper.pdf" | absolute_url}})


[pdf仓库地址](https://github.com/yang-jq/yang-jq.github.io/tree/master/pdfs/paper.pdf)





- **Step 3**：创建你的博客：进入自己的Github页面，点击右上角的`+` &rarr; `Import Repository` &rarr; 在`Your old repository's clone URL`填入Theme仓库URL：`https://github.com/userid/jekyll-theme-next` &rarr; 在`Your new repository details`的Name处填入`userid.github.io`。
- **Step 4**：你的个人博客现已成功上线。在浏览器地址栏输入`https://userid.github.io`尝试访问吧！示例：[我的个人博客](https://yang-jq.github.io/)。

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
