---
title: 测试Font Awesome字体
published: true
updated: 2018-06-11
---

Font Awesome图标

site title: {{site.title}}

Github link: {{site.social.GitHub}}

Github icon: {{site.social_icons[GitHub]}}

Github icon: <i class="fa fa-fw fa-{{ site.social_icons.GitHub | default: 'globe' | downcase }}"></i>

Github icon2: <i class="fa fa-fw fa-github"></i>
