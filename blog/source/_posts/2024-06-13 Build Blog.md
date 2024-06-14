---
title: Build Blog
categories:
  - hexo
tags:
  - blog
abbrlink: 21666
date: 2024-06-13 18:31:55
---

这是测试文档,用来记录hexo-next主题的配置。

<!--more-->

# LocalSearch 搜索功能

## 安装搜索插件

 `hexo-generator-searchdb`

在博客根目录下执行以下命令：

```shell
& npm install hexo-generator-searchdb --save
```

## 配置博客

安装完成，编辑博客配置文件：`_config.yml`

```yml
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```

## 配置主题

Next 主题自带搜索设置，编辑主题配置文件：`_config.yml`

找到文件中 Local search 的相关配置，设为 `true`

```yml
# Local search
local_search:
  enable: true
```

# 分类，标签

还记得_config.yml中有关于meau的设置把。我们如果想将文章分类以及添加标签的话。首先在根目录执行 hexo new page categories。之后你会发现在博客根目录下source文件夹会生成一个categories文件夹。我们进入这个文件夹。用VSCODE打开里面的index.md进行编辑，在当中添加type类型。

---
```markdown
---
title: categories
date: 2020-02-19 22:27:43
type: categories
---
```

标签的操作也是类似这样。输入指令 hexo new page tags。接下来编辑index.md这个文件即可。添加type属性即可。

以上完成后我们就可以在文章中添加分类以及标签了。类似这样：

---
```markdown
---
title: hexo+next主题配置
date: 2020-03-04 23:22
categories: hexo博客主题配置
tags: Next主题美化
mathjax: true
---
```



mathjax: true
---
1
2
3
4
5
6
7
这样我们就可以查看我们自己文章的分类以及标签了。

# 评论功能


https://yashuning.github.io/2018/06/29/hexo-Next-%E4%B8%BB%E9%A2%98%E6%B7%BB%E5%8A%A0%E8%AF%84%E8%AE%BA%E5%8A%9F%E8%83%BD/

# 首页只显示文章摘要

以前那种每页显示固定字数的选项没了，现在手动设置：

1. 整体设置 NexT的 _config.yml
   将`excerpt_description: true`设为`true`

2. 在每个文章中插入`<!--more-->`,然后首页只显示该行以上的部分。

   # 访客统计

   next的_config.yml中busuanzi_count的enable设为true即可。

```yml
# Show Views / Visitors of the website / page with busuanzi.
# For more information: http://ibruce.info/2015/04/04/busuanzi/
busuanzi_count:
  enable: true
  total_visitors: true
  total_visitors_icon: fa fa-user
  total_views: true
  total_views_icon: fa fa-eye
  post_views: true
  post_views_icon: far fa-eye
```

