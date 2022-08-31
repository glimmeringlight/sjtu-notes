# 贡献指南

本站所有内容都开源在[Github代码仓库](https://github.com/felixchen0707/sjtu-iBME)中。如果你想要贡献你自己的内容，也在此处进行。以下介绍一些贡献前你可能需要了解的事项。

## Markdown支持度

+ [Common Mark](https://commonmark.org/help/)
+ 数学公式（本站使用MathJax来支持$\LaTeX$语法）
+ 脚注
+ html语法
+ 目录
+ 表格
+ 高亮
+ 删除线
+ 上下标
+ 任务列表

## 修改原有内容流程

+ 方式1
  
  进入你想要修改的文章页面，点击右侧的编辑按钮，直接修改md文件内容。

+ 方式2
  
  fork本文[源码仓库](https://github.com/felixchen0707/sjtu-iBME)，在docs目录下找到文章对应的md文件并修改。

修改完成后提交pull request，如无特殊情况，我们会合并你的代码，而后自动触发Vercel部署。片刻之后，你就能在本站访问到你发布的内容。

## 发布新内容流程

fork本文[源码仓库](https://github.com/felixchen0707/sjtu-iBME)，在docs目录下，根据你的文章所属分类，进入相应目录新建md文件。md文件的一级标题将作为侧边栏显示的标题。完成创作后提交pull request，我们将尽快审核内容并在审核通过后合并代码，Vercel将自动部署。
