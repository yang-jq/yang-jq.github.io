---
title: 你的博客已上线——基于Jekyll和Github Pages
layout: post
excerpt_separator: <!--more-->
categories: [Github Pages, Jekyll]
tags: [Github Pages, Jekyll]
published: true
permalink: /start-blogging.html
---


[Jekyll](https://jekyllrb.com/)([中文主页](https://www.jekyll.com.cn/))是将Markdown等轻量化标记语言编写的文本转换为静态网页的工具，而[Github Pages](https://pages.github.com/)是Github提供的静态网页托管服务。既有生成工具，又有托管服务，两者结合就可以便捷地创建个人博客或项目主页。


<!--more-->

### 挑选模板
从零开始亲手创建精致的个人博客当然需要耗费不少精力和时间，但幸好已经有不少优秀的开源博客模板可供直接选用。此处列举了一些：

|模板名称|模板预览|
|:---:|:---:|
|[NexT](https://github.com/simpleyyt/jekyll-theme-next)([主页](http://theme-next.simpleyyt.com/))|[NexT预览]({{"/blog_images/start-blogging/NexT_preview.png" | absolute_url}})|
|[TeXt](https://github.com/kitian616/jekyll-TeXt-theme)([主页](https://tianqi.name/jekyll-TeXt-theme/))|[TeXt预览]({{"/blog_images/start-blogging/TeXt_preview.png" | absolute_url}})|
|[Flexible](https://github.com/artemsheludko/flexible-jekyll)|[Flexible预览]({{"/blog_images/start-blogging/Flexible_preview.png" | absolute_url}})|
|[Github官方模板](https://pages.github.com/themes/)|[官方预览]({{"/blog_images/start-blogging/Official_preview.png" | absolute_url}})|
|[Jekyllthemes.org](http://jekyllthemes.org/)|[网站预览]({{"/blog_images/start-blogging/Jekyllthemes_org.png" | absolute_url}})|
|[Jekyll-themes.com](https://jekyll-themes.com/)|[网站预览]({{"/blog_images/start-blogging/Jekyll-themes_com.png" | absolute_url}})|

下面以NexT模板为例搭建博客。
- **Step 1**：注册[Github](https://github.com/)账号，Github用户名记为`userid`。
- **Step 2**：将NexT模板仓库(Repository)Fork到你的Github空间，将刚Fork到的NexT仓库更名为：`userid.github.io` (`NexT仓库页面` &rarr; `Settings` &rarr; `Rename`)
- **Step 3**：你的博客现已成功上线。在浏览器地址栏输入`https://userid.github.io`尝试访问吧。[[本人博博客]](https://yang-jq.github.io/)。

### 定制版面
你可能需要调整博客版面以符合你的审美。调整版面需要修改`_config.yml`文件，可以直接在博客仓库里在线修改。但在以后的写作中，通常是在本地完成撰写后，再通过Git命令或Github Desktop推送到Github，所以还是趁现在把需要用到的工具安装上吧。
- **Step 1**：安装[Github Desktop](https://desktop.github.com/)，并通过Github账户登录，将博客仓库下载到本地。
- **Step 2**：使用文本编辑器修改`_config.yml`全局配置文件，关于NexT主题的配置项可参考[NexT主页](http://theme-next.simpleyyt.com/)的说明：

|常用配置项|功能说明|可选值|示例|
|:---:|:---:|:---:|:---:|
|`scheme`|版面外观|`Muse`(默认)/`Mist`/`Pisces`|`scheme: Pisces`|
|`language`|语言|`en`/`zh-Hans`/'ja'等10种语言|`language: zh-Hans`|
|`menu`|菜单|参考[NexT主页-快速开始](http://theme-next.simpleyyt.com/getting-started.html)|可自定义菜单|
|`title`|博客名称|字符串|`title: my blog`|
|`avatar`|头像|图片链接|`avatar: /image/avatar.png`|
|`rss`|RSS订阅|`false`/留空/具体地址|`rss: false`，即不启用|
|`social`|侧边栏社交链接|参考[NexT主页-主题配置](http://theme-next.simpleyyt.com/theme-settings.html)，[Font Awesome图标](http://fontawesome.dashgame.com/)| `GitHub: https://github.com/userid`|
|`highlight_theme`|代码高亮样式|`normal`/`night`/`night eighties`/`night blue`/`night bright`|`highlight_theme: normal`|
|`baidu_analytics`|添加百度统计功能后，可自行登陆查看个人博客的访问情况|参考NexT主页|`baidu_analytics: baidu_id`|
|`use_motion`|动画效果|`true`(默认)/`false`|`use_motion: false`|
|`busuanzi_count`|访问统计|`true`/`false`，参考[NexT主页-第三方服务](http://theme-next.simpleyyt.com/third-party-services.html)|`enable: true`|
|`add_this_id`|[Addthis分享功能](http://theme-next.simpleyyt.com/third-party-services.html)|Addthis的用户id|`add_this_id: addthis_id`|
|`local_search`|站内搜索|`true`/`false`|`enable: true`|
|`post_meta`|显示创建、更新、分类信息(尚未完善)|`true`/`false`|`created_at: true`|
|`post_wordcount`|显示字数、阅读时间(尚未完善)|`true`/`false`|`wordcount: true`|
|`custom_logo`|logo图案|`true`/`false`|`enable: true`，`image: /logo.png`|
|`mathjax`|数学公式|`true`/`false`|`enable: true`|
|`version`|版本，在文档最后一行|字符串|NexT的版本号|

- **Step 3**：修改`_config.yml`配置文件后，在Github Desktop上把修改推送到博客仓库，配置才能生效：`Commit to master` &rarr; `Push origin`。


### 开始创作
定制好版面后，就可以开始创作了。Jekyll支持使用[Markdown](http://www.markdown.cn/)语言来撰写博文，它会将每一篇`.md`文章自动转换成`.html`格式进行发布。为了撰写`.md`文章时能够实时显示排版效果，此处推荐Github开发的[Atom](https://atom.io/)编辑器。

- **Step 1**：安装[Atom](https://atom.io/)编辑器，关闭Markdown-preview插件(无法显示数学公式)后，安装Markdown-preview-plus增强插件：
  - `File` &rarr; `Settings` &rarr; `Packages` &rarr; `markdown-preview` &rarr; `Disable`；
  - `File` &rarr; `Settings` &rarr; `Install` &rarr; `markdown-preview-plus`。
- **Step 2**：在博客仓库的`_posts`下新建`year-month-day-title.md`文档，在`.md`文档中写入内容，然后通过Github Desktop推送到线上的博客仓库，即完成博文的发布。

需要说明的是，[Jekyll](https://www.jekyll.com.cn/)会将每个`.md`文档开头两行`---`之间的信息看作是`YML`头信息，然后根据头信息中的选项进行相应处理，常用的选项如下：

|选项|作用|示例|
|:---:|:---:|:---:|
|`title`|博文标题|`title: 第一篇博客`|
|`layout`|布局|`layout: post`, 其它选项可参考`_layouts`中的文件名|
|`excerpt_separator`|摘要截取符，在截取符之前的文字将作为文章的摘要|`excerpt_separator: <!--more-->`|
|`categories`|为文章分类|`categories： [Jekyll, Github]`|
|`tags`|为文章加标签|`tags: [Jekyll, Github]`，类似于`category`的功能|
|`published`|是否发布|`published: true`|
|`premalink`|永久链接，用于从别的页面对当前页面进行引用|`premalink: /start-blogging.html`|
|`comments`|开启或关闭评论功能|`comments: false`|

例如，在本地博客仓库的`_posts`文件夹内新建一个`2018-06-07-start-blogging.md`的文件，然后写入
```
---
title: 开始你的博客之旅
layout: post
tags: [Blog, Jekyll]
published: true
excerpt_separator: <!--more-->
premalink: /start-blogging.html
---
文章正文：
一切从这里开始...
```

### 避坑指南(陆续更新...)
#### 插入图片
假设图片的路径在`本地博客仓库/images/pic1.png`，用以下命令可将图片插入到文章中：
```
![图1]({{"/images/pic1.png" | cmd_str}})  # 其中 cmd_str = absolute_url
```
需要注意的是，目录不能以`_`开头，即不能将图片放在`/_images/pic1.png`内，否则将无法识别。
#### 插入附件
假设需要向文章中插入`.pdf`文件，可用跟插入图片类似的方法：
```
[点此下载]({{"/pdfs/paper.pdf" | cmd_str}})  # 其中 cmd_str = absolute_url
```
#### 引用文章
假设需要从一篇文章`/article1.md`中链接到另一篇文章`/article2.md`，首先在`/article2.md`的`YML`头信息中设置永久链接：`premalink: /article2.html`，那么可通过以下命令实现引用：
```
[我的简介]({{"/article2.html" | cmd_str}})  # 其中 cmd_str = absolute_url
```
