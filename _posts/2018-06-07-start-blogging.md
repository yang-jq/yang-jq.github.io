---
title: 博客上线指南——基于Jekyll和Github Pages
layout: post
excerpt_separator: <!--more-->
categories: [Github Pages, Jekyll]
tags: [Github Pages, Jekyll]
published: false
permalink: /start-blogging.html
updated: 2018-06-11
---

[Jekyll](https://jekyllrb.com/)([中文主页](https://www.jekyll.com.cn/))是将Markdown等轻量化标记语言编写的文本转换为静态网页的工具，而[Github Pages](https://pages.github.com/)是Github提供的静态网页托管服务。生成工具与托管服务两者的结合就可以便捷地创建个人博客或项目主页。
<!--more-->

## 挑选模板
从零开始亲自创建精致的个人博客当然需要耗费不少精力和时间，但幸好已经有不少优秀的开源博客模板可供直接选用。此处列举了一些：

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
- **Step 2**：将[NexT模板仓库](https://github.com/simpleyyt/jekyll-theme-next)Fork到你的Github空间，将刚Fork到的NexT仓库更名为：`userid.github.io` (操作流程：`NexT仓库页面` &rarr; `Settings` &rarr; `Rename`)
- **Step 3**：你的博客现已成功上线。在浏览器地址栏输入`https://userid.github.io`尝试访问吧。[[本人博客]](https://yang-jq.github.io/)。

## 定制版面
你可能需要调整博客版面以符合你的审美。调整版面需要修改`_config.yml`文件，可以直接在博客仓库里在线修改。但在以后的写作中，通常是在本地完成文稿后，再通过Git命令或Github Desktop推送到Github，所以趁现在就把需要用到的工具安装上吧。
- **Step 1**：安装[Github Desktop](https://desktop.github.com/)，并通过Github账户登录，将博客仓库下载到本地。
- **Step 2**：使用文本编辑器修改`_config.yml`全局配置文件，关于NexT主题的配置项可参考[NexT主页](http://theme-next.simpleyyt.com/)的说明。
- **Step 3**：修改`_config.yml`配置文件后，在Github Desktop上把修改推送到博客仓库，配置才能生效。(操作流程：`Github Desktop` &rarr; `Commit to master` &rarr; `Push origin`)。

此处列举了一些常用配置项：

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

## 开始创作
定制好版面后，就可以开始创作了。Jekyll支持使用[Markdown](http://www.markdown.cn/)语言来撰写博文，它会将每一篇`.md`文章自动转换成`.html`格式进行发布。为了撰写`.md`文章时能够实时显示排版效果，此处推荐Github开发的[Atom](https://atom.io/)编辑器。

- **Step 1**：安装[Atom](https://atom.io/)编辑器，关闭Markdown-preview插件(因其无法显示数学公式)后，安装Markdown-preview-plus增强插件：
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
|`updated`|更新时间|`updated: 2018-06-10`|

目前，`updated`字段还不支持自动更新，需要手动修改日期，同时在`_config.yml`配置文件中设置：
```
post_meta:
  updated_at: true
```


例如，在本地博客仓库的`_posts`文件夹内新建一个`2018-06-07-start-blogging.md`的文件，然后写入以下内容并通过Github Desktop推送到Github，即可发布一篇标题为“开始你的博客之旅”的文章。
```
---
title: 开始你的博客之旅
layout: post
tags: [Blog, Jekyll]
published: true
excerpt_separator: <!--more-->
premalink: /start-blogging.html
updated: 2018-06-11
---
正文从此处开始...首篇博文...
```

## 常用功能(陆续更新...)
### 插入图片
假设图片的路径在`本地博客仓库/images/pic1.png`，用以下命令可将图片插入到文章中：
```
![图1]({~{"/images/pic1.png" | absolute_url}~})  # 把"~"号去掉
```
需要注意的是，目录不能以`_`开头，即不能将图片放在`/_images/pic1.png`内，否则将无法识别。
### 插入附件
假设需要向文章中插入`.pdf`文件，可用跟插入图片类似的方法：
```
[点此下载]({~{"/pdfs/paper.pdf" | absolute_url}~})  # 把"~"号去掉
```
### 引用文章
假设需要从一篇文章`/article1.md`中链接到另一篇文章`/article2.md`，首先在`/article2.md`的`YML`头信息中设置永久链接：`premalink: /article2.html`，那么可通过以下命令实现引用：
```
[我的简介]({~{"/article2.html" | absolute_url}~})  # 把"~"号去掉
```

### 插入图标
[Font Awesome](http://fontawesome.dashgame.com/)提供了将近700个高质量的矢量图标和公司商标。可通过以下代码段向文章中插入图标或商标。需要提醒的是，商标涉及专利或版权，使用需慎重。

- 默认样式
<br><i class="fa fa-github"></i>
```
<i class="fa fa-github"></i>
```
- 指定图标大小
<br><i class="fa fa-github" style="font-size:24px;"></i>
```
<i class="fa fa-github" style="font-size:24px;"></i>
```
- 指定图标颜色
<br><i class="fa fa-github" style="color:red;"></i>
```
<i class="fa fa-github" style="color:red;"></i>
```
颜色值可以指定为RGB值，比如`color:#8A2BE2`(<span style="color:#8A2BE2">紫</span>)。16种预定义的颜色名称为：<span style="color: aqua">aqua</span>， <span style="color: black">black</span>， <span style="color: blue">blue</span>，<span style="color: fuchsia">fuchsia</span>，<span style="color: gray">gray</span>，<span style="color: green">green</span>，<span style="color: lime">lime</span>，<span style="color: maroon">maroon</span>，<span style="color: navy">navy</span>，<span style="color: olive">olive</span>，<span style="color: purple">purple</span>，<span style="color: red">red</span>，<span style="color: silver">silver</span>，<span style="color: teal">teal</span>，<span style="color: white; background:black">white</span>，<span style="color: yellow">yellow</span>。

- 按比例缩放图标
<br><i class="fa fa-github"></i> <i class="fa fa-github fa-lg"></i> <i class="fa fa-github fa-2x"></i>
```
<i class="fa fa-github"></i>  # 原始大小
<i class="fa fa-github fa-lg"></i> # large尺寸
<i class="fa fa-github fa-2x"></i>  # 2x尺寸
```

- 固定宽度
<br>使用`fa-fw`将图标设置为一个固定宽度，主要用于不同宽度图标无法对齐的情况，尤其在列表或导航时实现对齐。
<br><i class="fa fa-home fa-fw"></i>
<br><i class="fa fa-book fa-fw"></i>
<br><i class="fa fa-pencil fa-fw"></i>
<br><i class="fa fa-cog fa-fw"></i>
```
<i class="fa fa-home fa-fw"></i>
<i class="fa fa-book fa-fw"</i>
<i class="fa fa-pencil fa-fw"></i>
<i class="fa fa-cog fa-fw"></i>
```



- 图标旋转动画
<br>使用`fa-spin`可以使任意图标旋转，使用`fa-pulse`则进行8方位旋转：
<br><i class="fa fa-circle-o-notch fa-spin"></i>
<i class="fa fa-refresh fa-spin"></i>
<i class="fa fa-cog fa-spin"></i>
<i class="fa fa-spinner fa-pulse"></i>
```
<i class="fa fa-circle-o-notch fa-spin"></i>
<i class="fa fa-refresh fa-spin"></i>
<i class="fa fa-cog fa-spin"></i>
<i class="fa fa-spinner fa-pulse"></i>
```

- 旋转及翻转图标
<br>使用`fa-rotate-*`和`fa-flip-*`可以对图标进行任意旋转和翻转：
<br><i class="fa fa-shield"></i>：原始样式
<br><i class="fa fa-shield fa-rotate-90"></i>：旋转90度
<br><i class="fa fa-shield fa-rotate-180"></i>：旋转180度
<br><i class="fa fa-shield fa-rotate-45"></i>：旋转45度
<br><i class="fa fa-shield fa-flip-horizontal"></i>：水平翻转
<br><i class="fa fa-shield fa-flip-vertical"></i>：垂直翻转
```
<i class="fa fa-shield"></i>：原始样式
<i class="fa fa-shield fa-rotate-90"></i>：旋转90度
<i class="fa fa-shield fa-rotate-180"></i>：旋转180度
<i class="fa fa-shield fa-rotate-45"></i>：旋转45度
<i class="fa fa-shield fa-flip-horizontal"></i>：水平翻转
<i class="fa fa-shield fa-flip-vertical"></i>：垂直翻转
```

- 组合图标
<br>使用`fa-stack`作为父容器将多个图标组合后使用：
<br><i class="fa fa-square-o fa-1x"></i> +
<i class="fa fa-twitter fa-1x"></i> =
<span class="fa-stack fa-lg">
  <i class="fa fa-square-o fa-stack-2x"></i>
  <i class="fa fa-twitter fa-stack-1x"></i>
</span>
```
<span class="fa-stack fa-lg">
  <i class="fa fa-square-o fa-stack-2x"></i>
  <i class="fa fa-twitter fa-stack-1x"></i>
</span>
```

### Emoji表情
<br> :smile: :flushed: :joy: :triumph: :white_flower: :sunny:
```
:smile: :flushed: :joy: :triumph: :white_flower: :sunny:
```
更多的Emoji表情代码请参考[Emoji cheat sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet/)

### 字数统计
在`_config.yml`配置文件中设置：
```
post_wordcount:
  wordcount: true
  separated_meta: false
```

### 参考文献
1. Jekyll主页：[https://jekyllrb.com/](https://jekyllrb.com/)，[中文主页](https://www.jekyll.com.cn/)。
2. Github Pages：[https://pages.github.com/](https://pages.github.com/)。
3. NexT模板仓库：[https://github.com/Simpleyyt/jekyll-theme-next](https://github.com/Simpleyyt/jekyll-theme-next)。
4. Font Awesome主页：[http://fontawesome.dashgame.com/](http://fontawesome.dashgame.com/)。
5. Emoji表情代码主页：[https://www.webpagefx.com/tools/emoji-cheat-sheet/](https://www.webpagefx.com/tools/emoji-cheat-sheet/)。
