---
layout: post
title: "github + jekyll + markdown 打造自己的博客"
description: "最近开通了自己的博客，记录一下打造自己的博客的历程。"
date:  2014-08-31 12:27:55
categories: Memory
tag: [github, jekyll, markdown]
---
谈谈自己用github pages, jekyll, markdown来打造自己博客的历程。

## github pages

>[github pages](https://pages.github.com/)  空间免费，博客，托管于[github](https://github.com/)

>使用git同步管理文章，版本控制嵌入博客书写中

>[自定义域名](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages)

---

## jekyll

>[jekyll](http://jekyllrb.com/)的核心其实是一个文本转换引擎。

>允许本地服务器调试

>支持markdwon等多种格式来书写博客

---

## markdown

>[markdown](http://daringfireball.net/projects/markdown/syntax)实质是一种标记语言。 (中文版语法说明)[http://wowubuntu.com/markdown/]

>易读易写。Markdown适合书写，而HTML适合发布。

---

## 命令

### 使用github page

1. 在github创建自己的Repository，命名格式为username.github.io
2. git clone https://github.com/username/username.github.io 
3. cd username.github.io; echo "Hello World" > index.html
4. 使用username.github.io的域名就可以访问自己的主页了

### 使用jekyllrb

1. 安装Ruby, RubyGems
2. gem install jekyllrb
3. jekyll new myblog
4. cd myblog; jekyll serve
5. http://localhost:4000 即可访问jekyll生成的静态网站

### github+jekyll

前面只是提到github和jekyll各自的功能，如何把它们结合起来呢。

1. cd myblog; git init;
2. git remote add (name) (https://github.com/username/username.github.io)
3. git pull （拉取远程库的内容合并到当前库)
4. 在使用git将所有修改在本地提交后，使用git push origin master将本地库同步至github仓库。
5. 到了这里，你已经可以在公网访问到自己使用jekyll打造的博客了。
6. 前面的所有步骤都只是第一步，博客的内容本身才是最重要的，多写写博客比打造好看的博客来得更重要。

---

## 参考文章

>[搭建一个免费的，无限流量的Blog----github Pages和Jekyll入门](http://www.ruanyifeng.com/blog/2012/08/blogging_with_jekyll.html)

>[使用github+jekyll搭建blog环境，完美替代wordpress](http://www.heiniuhaha.com/lessons/2012/08/09/use-jekyll-build-blog/)
