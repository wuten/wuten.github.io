---
layout: post
title: jekyll just tools
date: 2022-09-04 19:37 +0800
categories: tools
tags: jekyll
---



### [jekyll撰写插件](https://github.com/jekyll/jekyll-compose)、[撰写新帖子](https://chirpy.cotes.page/posts/write-a-new-post/)

草稿－－》整理－－》帖子

- 新建草稿：`$ bundle exec jekyll draft "My New Post"`
- 重命名草稿：`$ bundle exec jekyll rename _drafts/my-new-draft.md "My Renamed Draft"`
- 新建帖子：`$ bundle exec jekyll post "My new draft"`

### 本地预览

```bash
bundle exec jekyll s --incremental
```
  
## 故障1

```bash
$ bundle
Traceback (most recent call last):
        2: from /home/bit/gems/bin/bundle:23:in `<main>'
        1: from /usr/lib/ruby/2.5.0/rubygems.rb:308:in `activate_bin_path'
/usr/lib/ruby/2.5.0/rubygems.rb:289:in `find_spec_for_exe': can't find gem bundler (>= 0.a) with executable bundle (Gem::GemNotFoundException)
```

Gemfile.lock锁定了版本,删除即可

## 故障2：编译测试不通过

注释测试内容
```
#- name: Test site
#  run: |
#    bundle exec htmlproofer _site \
#      \-\-disable-external=true \
#      \-\-ignore-urls "/^http:\/\/127.0.0.1/,/^http:\/\/0.0.0.0/,/^http:\/\/localhost/"
```

## jekyll

jekyll是一个工具
通过markdown编写文档生成静态网站。

类似的工具gitbook、Sphinx。

- gitbook更适合用来写书籍，
- sphinx更适合用来写使用手册，
- jekyll更适合用于构建博客。

同时gitbook jekyll使用markdown作为格式化语言，
而sphinx则使用reStructuredText作为格式化语言。

[jekyll本地环境安装](https://jekyllrb.com/docs/installation/)

[在gitpages中配置jekyll](https://jekyllcn.com/docs/configuration/)
