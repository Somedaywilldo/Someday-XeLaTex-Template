# Someday's XeLaTeX Template

## NOTICE

### Fortunately 2019.04.25

非常感谢两位18级的级同学 **lawye, nikkukun** 的贡献，使得这个模板重新焕发了生机，并且更加严格的按照冯如杯标准格式进行了修改，希望之后该模板能被冯如杯组委会，**经过与作者联系**之后而采用，从而节省广大同学在调整冯如杯格式上所浪费的时间。

Someday也欢迎各位北航/非北航同学，使用该模板进行其他论文写作。

Someday认为两位新同学的主文件更好一些，以前的文件 **main.tex** 被移动至 **old/** 下，之后将被清理，新的主文件为 **FRBKeji.tex** ，Latex符号对应表和冯如杯格式规范移动至 **Reference/** 下。

### Unfortunately 2019.03.06

    在一次非常不愉快的维权事件之后，我决定不再更新维护该模板，但依旧鼓励大家使用并自己修改。请大家注意版权意识，如果用于个人用途，请随意。如果用于直接用于大规模散布，请征得作者同意。因为作者从未接受任何组织的委托制作该模板，且该模板为作者完全原创，并非改良而成，理应享有全部的著作权。但如果因为模板问题导致比赛失利，这个责任，作者不应该、也无法承担，这些，也清清楚楚地写在BSD开源协议中。
    
    对于做这件事的同学，开源协议不是用来允许你随便复制粘贴的，就改个标题就敢直接发布到我自己学校当官方模板，留着我的公众号链接和联系方式，出了错难道全校同学不会有人找我么？不合格怎么办？我还得帮着他们改bug不成？你们的所作所为，直接让全校同学们失去了一次使用LaTeX模板参赛的机会，2019年中，又将有无数的同学将宝贵的时间耽误在调整格式上，包括我自己。
    
    对著作权的充分尊重，是科技工作者的基本素养，也是开源社区的精神所在，我对你们深表失望。
    
    我本想为学校做点贡献，让使用LaTeX成为校内一种风尚，节约大家调整格式的时间，没想到这个事来的如此突然。看来今年无望，然而在校时日已经不多，望北航在LaTeX开源贡献方面后继有人。

## Someday的XeLaTeX中文模板

首先，如果你是初学者，不要一进来就发现是XeLaTeX而不是LaTeX，然后就匆匆离开。XeLaTeX本身就是LaTeX的一个分支，很多命令可以通用，XeLaTeX的优点是支持第三方字体。

现在，欢迎你使用Someday出品的TeX模板，因为网上很多模板下载下来根本无法使用，而且最最让人头痛的就是LaTeX对中文的支持很不友好，所以我采用了XeLaTeX，因为可以导入第三方字体。然后我从头学习，从配置到尝试，自己搭建了一个模板，希望对你有帮助！

### 需要的宏包

* `ctex`,也包含了ctex中需要的宏包
* `xeCJK` 中文支持
* `amssymb` 数学公式
* `amsmath` 数学公式支持
* `listings` 提供tex中的列表
* `graphicx` 插入图片
* `multicol` 用于回车换行
* `xcolor` 调整文件字体颜色等
* `geometry` 调整页边距
* `fontspec` 调整字体大小
* `setspace` 控制标题前后段间距
* `times` 英文采用`Times New Rome`字体
* `fancyhdr` 用于控制页眉页脚格式
* `float` 浮动体, 用于排版图片等
* `titlesec` 设置标题前后间距

以上的所有宏包都需要安装最新版本, 否则会编译失败~~你可以尝试删除某些宏包以查看效果会发生什么变化~~

### 可选编译方式：

#### 1、Sublime Text：

Someday使用的是Mac系统，Sublime Text2用Package Control安装Latextool插件后进行编译，编译模式为XeLaTeX，可以直接编译。

lawye和nikkukun使用win10系统, 该模板在win10+texlive2018 环境下编译成功.

#### 2、在线TeX IDE：

在[sharelatex](www.sharelatex.com)网站上也可以直接编译，编译选项为XeLaTeX。
[Overleaf](https://cn.overleaf.com/)也是推荐的一款在线编辑器.

#### 3、命令行编译：

在TeXLive2016环境下，编译命令如下：

```cmd
cd  <模板根目录>
xelatex main.tex
```

在TeXLive2018环境下, 如需生成参考文献, 应采用以下命令

```cmd
cd  <模板根目录>
xelatex main.tex
bibtex main.tex
xelatex main.tex
xelatex main.tex

```

#### 4、本地IDE编译：

本机已经安装TeX套装、TeX IDE等亦可编译，注意编译选项为XeLaTeX即可。

lawye采用vscode+TeXLive方式编译, 配置好以后, 只需要按快捷键即可

### 模板结构：

#### 1、`main.tex`或`FRBKeji.tex`

`main.tex`是整个模板的灵魂，所有的宏包导入，格式设置，页面设置请在该文件中完成，模板中已经提供了页面、中文字体、中文字号、页码、页眉页脚、目录、章节标题样式、章节标号等设置选项。并且提供了封面、图片、表格、引入字体，引入文件、插入代码片等样例。

`main.tex`使用`\documentclass{ctexart}`作为文档类别的属性，这是Chinese Tex Article的缩写，是一个现成的模板，目录、摘要等关键词的默认语言就是中文。

`main.tex`的编译结果就是`main.pdf`，你可以先看看自己对这个结果是否满意。

#### 2、字体文件夹

目录名：`fonts`

你自己的字体文件直接放在根目录下就可以了，在导言区设置以下命令：

中文字体：`\setCJKmainfont[Path=fonts/,BoldFont=simhei.ttf,ItalicFont=simkai.ttf]{simsun.ttc}`

中文字体涵盖黑体、宋体、楷体、仿宋

英文字体：`\setmainfont[Path=fonts/]{Times New Roman.ttf}`

`\setmonofont[Path=fonts/]{Courier New.tff}`

这样设置中文字体后，

文本默认的字体是宋体，若调用黑体：`\textbf{黑体写在这里}`，调用楷体：`\textit{楷体写在这里}`，调用仿宋：`\texttt{仿宋写在这里}`。

#### 3、图片文件夹

目录名：`include_picture`

将所需图片放入该目录下，按如下方式使用：

`\includegraphics[scale=0.4]{include_picture/picture.jpg}`或

```latex
\begin{figure}[H]
    \centering
    \includegraphics[scale=0.4]{include_picture/picture.jpg}
    \caption{图的标题}
\end{figure}
```

#### 4、引用文章文件夹

目录名：`include_tex`

将需要引用的.tex文件放入该目录下，注意引用的tex只保留文章内容，不需要导言区以及各种格式设置选项，设置格式请在main.tex中完成，样例可参照在`include_tex`下的`include_section.tex`文件。

```latex
\input{include_tex/include_text} %使用input将在原位置显示
\include{includetex} %使用include将另起一页显示
```

#### 5、参考文献bibtex

文件名: `library.bib`

将参考文献的bibtex信息复制到该文献中,在正文部分使用`\citeup{}`命令引用即可.

    注意事项: 采用bibtex的结果是编译时需要使用4次编译: xelatex->bibtex->xelatex->xelatex 才可以正确显示参考文献

### 作者的一点期许：

1. 希望这个模板能对你有帮助，作为使用或者学习的好素材。
2. 希望你在使用时保留`main.tex`的这些注释：

```latex
    %Welcome! This is Someday's XeLaTeX Template.
    %Developer: Someday（BUAA-SCSE）
```

**记住，官方的说明文档（Documentation）永远是最好的教程。**

## 尊重Someday的著作权

Someday开放个人用途的使用权，如果它真的对你起了很大的帮助，可以在见到我的时候请我喝咖啡。

### 后记：

为什么网上流传的LaTeX模板很多，而我还是要“重新发明轮子”，这是因为，网上绝大多数模板缺少必要的说明，除非你理解每行代码的含义，否则还是无法使用。或者有的模板过于完备或者繁杂，这为通常任务很急的论文写作带来了不小的麻烦，而且我希望自己能慢慢成长为一个LaTeX高手，所以，我自己摸索开发了一个模板。想享受LaTeX带来的便利，直接使用这个模板就好了，但如果你想真正领悟其中的含义，那就自己再发明一次轮子吧!~

### 注意：如果你是我航学子，并因冯如杯使用该模板

首先，我劝你是别用，除非冯如杯官方自己发过了模板。

该模板目前满足了冯如杯论文的如下要求：

#### 1、字体字号

论文题目:二号,华文中宋体加粗,居中。
章标题:三号,黑体,居中。

节标题:四号,黑体,居左。

正文:小四号,中文字体为宋体,西文字体为 Times New Roman 体,首行缩进,两端对齐。

页码:五号宋体数字和字母,Times New Roman 体。

#### 2、页边距

上边距:25mm;下边距:25mm;左边距:30mm;右边距 20mm。

#### 3、页眉

页眉用小五号宋体字，居中，页眉标注从论文主体部分开始(绪论或第一章)。

格式已经符合，请自行修改内容。

#### 4、页码

页码先在摘要以及目录部分用罗马数字编码, 后从主体部分开始用五号阿拉伯数字连续编码,页码位于页脚居中。封面、题名页不编页码。

摘要、目录、图标清单、主要符号表用五号小罗马数字连续编码,页码位于页脚居中。

#### 5、封面

样式基本符合，图的位置已经按照word模板中的空行设置。

#### 6、目录

我航对目录其实没有格式上的要求，可以放松心使用。

其它要求，请等待作者不断更新，未完待续。

## UPDATE

### UPDATE 2019.04.14

lawye和nikkukun继续维护模板. 新增内容:

1. 添加文件`FRBKeji.tex`以用于冯如杯学术科技竞赛
2. 修改`README.MD`, 修正语法错误, 添加继续更新信息
3. 添加自定义宏包`gbt7714`, 用于参考文献格式的正确显示
4. 添加`library.bib`用于存储参考文献信息
5. 修改了一些编译方式.
6. 修改页眉以及字号以及目录格式

### UPDATE 2017.09.08

经123学长指正，Someday于2017.09.08进行一次重要更新，内容包括：

1. 对中文字号的设置命令进行了修改，使用方法不变。
2. 对仿宋字体所在的fontstyle进行了修改，以适应fontspec宏包。
3. 将取消首页页码的命令改为：pagenumbering{gobble}

以上修正解决了以前版本中编译报错问题，当前版本在TeXLive2016环境下已经可以一次编译成功。

编译命令如下：

```cmd
cd  <模板根目录>

xelatex main.tex
```

### UPDATE 2017.07.14

1. 增加LaTeX符号对应表----LaTeX simbols table.pdf
2. 增加了“注意：如果你是我航学子，并因冯如杯使用该模板”说明