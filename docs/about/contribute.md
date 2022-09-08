# 贡献指南

本站所有内容都开源在[Github代码仓库](https://github.com/felixchen0707/sjtu-iBME)中。如果你想要贡献你自己的内容，也在此处进行。以下介绍一些贡献前你可能需要了解的事项。

## Markdown支持度

本站已配置了较为完备的Markdown插件，利用Markdown，你可以轻松写作出一篇布局合理的文章。

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
+ 代码块

## 修改原有内容流程

=== "方式1"

    进入你想要修改的文章页面，点击文章一级标题处的编辑按钮，即可立即跳转到本文的源码。你可以直接修改仓库源码内容，修改完成后发起pull request，等待代码合并即可。

=== "方式2"

    fork项目的[源码仓库](https://github.com/felixchen0707/sjtu-iBME)，在docs目录下找到文章对应的md文件并修改。本项目的目录结构为
    ```
    /docs/courses/年级/课号/Markdown文件
    ```
    修改完成后，发起pull request。

不论何种方式，发起pull request后，我们会确认代码的正确性。如果没有特殊情况，你的代码将会被合并至主仓库中。等待Vercel自动构建后，你可以访问本站来看到你的贡献了。

## 发布新内容流程

fork项目的[源码仓库](https://github.com/felixchen0707/sjtu-iBME)，根据目录结构`/docs/courses/年级/课号/Markdown文件`进入合适的目录下新建Markdown文件。Markdown文件的一级标题将作为侧边栏显示的标题。完成创作后提交pull request，我们将尽快review并合并代码或做出修改。待合并代码后，Vercel将自动部署。

对于新内容，请务必注意以下几点：

1. Markdown文件的命名**请遵循课号+序列号的命名方式**：例如`BME1201_03.md`表示课程**生物医学工程导论**的**第三篇文章**，这将利于保持网站url的规范性；
   
2. 文章的**一级标题**会被作为侧边栏显示的标题出现，所以请务必确保你的文章**以一级标题开头**。**一级标题就是你的文章标题**；
   
3. （可选）新建文章后，你可以前往`/mkdocs.yml`中的`nav`配置项添加你的文章路径。以下给出一段参考配置：例如需要添加`BME1201_15.md`，找到`BME1201 生物医学工程导论`，在后面的列表中加入你的文章路径即可。
```diff
# 全站导航栏
nav:
  - 开始:
    - index.md
    
  - 课程:
    - 大一课程:
      <snip>
    - 大二课程:
      <snip>
      - MATH1206 数理方法:
        - courses/grade2/MATH1206/MATH1206_01.md
      - BME1201 生物医学工程导论:
        - courses/grade2/BME1201/BME1201_01.md
+       - courses/grade2/BME1201/BME1201_15.md
      - BME1203 生物学导论:
        - courses/grade2/BME1203/BME1203_01.md
      <snip>
```
当然，如果你不清楚如何添加，我们**会帮助你完成这项工作**，你只需要在pull request的提交信息中备注“**未配置文章路径**”即可。
   
## 对于非文章内容的贡献

如果你贡献的内容不是文章内容，请在pull request中详细阐述**你的贡献内容**。对于非内容性的修改，我们可能需要更长的时间来确认而后合并代码。

## 内容扩充

本网站**具有很强的可扩展性**。除了课程评价，许多心得和分享都可以在合适的位置出现。如果你想要分享的内容找不到合适的地方发布，可以[联系我](mailto:felix_chen@sjtu.edu.cn)，**我们欢迎任何形式的贡献**。

## 更多问题

如果你有其他有关贡献的问题，你可以前往[Github Issues](https://github.com/felixchen0707/sjtu-iBME/issues)中提出，或者在此页面直接留言。
