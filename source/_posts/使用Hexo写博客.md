---
title: 使用Hexo写博客
categories:
  - 技术
tags:
  - Hexo
  - 博客
---
使用 Hexo 搭建博客，且采用 NexT 主题，详细介绍写一篇新博客的步骤。

## 创建新博客文章
   在终端里，切换到博客根目录（也就是 foleydang 目录），然后运行下面的命令来创建新的博客文章：

``` bash
cd /Users/bytedance/foleydang
hexo new "你的文章标题"
```

运行该命令后，Hexo 会在 source/_posts 目录下生成一个新的 Markdown 文件，文件名是你设置的文章标题。例如，创建名为 “新博客文章” 的文章：

## 编辑博客文章
   使用文本编辑器（像 Visual Studio Code、Sublime Text 等）打开刚生成的 Markdown 文件，文件开头会有类似下面的 Front - Matter 信息：

``` bash
---
title: 新博客文章
tags:
---
```
你可以按照需求补充或修改这些信息，比如添加 date（文章发布日期）、categories（文章分类）、tags（文章标签）等：

``` bash
---
title: 新博客文章
date: 2025-07-16
categories:
- 技术
  tags:
- Hexo
- 博客
---
```
接着在 Front - Matter 之后撰写文章内容，Markdown 语法支持标题、列表、图片、链接等常见格式。例如：

``` bash
---
title: 新博客文章
date: 2025-07-16
categories:
- 技术
  tags:
- Hexo
- 博客
---

## 引言
这是我的第一篇使用 Hexo 搭建的博客文章。

### 搭建过程
在搭建博客时，我使用了 Hexo 这个静态网站生成器，并且选择了 NexT 主题。具体步骤如下：
1. 安装 Hexo
2. 创建新的 Hexo 项目
3. 安装 NexT 主题
4. 配置博客信息

### 总结
通过这次搭建博客的经历，我对静态网站生成器有了更深入的了解。
```
## 本地预览文章
   在终端运行以下命令生成静态文件并启动本地服务器：

``` bash
hexo generate
hexo server
```
或者使用简写命令：

``` bash
hexo g
hexo s
```
启动成功后，在浏览器访问 http://localhost:4000 就能预览新写的博客文章。

## 部署博客到远程仓库
   若要将博客部署到 GitHub Pages 等远程仓库，需先在 _config.yml 文件里配置部署信息，当前配置如下：

``` bash
_config.yml
Apply
deploy:
type: git
repo: git@github.com:foleydang/foleydang.github.io.git
branch: master
```
配置完成后，在终端运行以下命令部署博客：

``` bash
hexo deploy
```
或者使用简写命令：


``` bash
hexo d
```
部署成功后，访问 https://foleydang.github.io 就能看到新发布的博客文章。