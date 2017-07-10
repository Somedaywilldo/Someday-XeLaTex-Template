# Someday's XeLaTeX Template

## Someday的XeLaTeX中文模板

首先，如果你是初学者，不要一进来就发现是XeLaTeX而不是LaTeX，然后就匆匆离开。XeLaTeX本身就是LaTeX的一个分支，很多命令可以通用，XeLaTeX的优点是支持第三方字体。

现在，欢迎你使用Someday出品的TeX模板，因为网上很多模板下载下来根本无法使用，而且最最让人头痛的就是LaTeX对中文的支持很不友好，所以我采用了XeLaTeX，因为可以导入第三方字体。然后我从头学习，从配置到尝试，自己搭建了一个模板，希望对你有帮助，有任何的Bug，及改进意见，欢迎联系作者：somedayjiayi@163.com



### 模板系统环境：

Someday使用的是Mac系统，Sublime Text2用Package Control安装Latextool插件后进行编译，编译模式为XeLaTeX，可以直接编译。

在www.sharelatex.com网站上也可以直接编译。



### 模板结构：

#### 1、main.tex

main.tex是整个模板的灵魂，所有的宏包导入，格式设置，页面设置请在该文件中完成，模板中已经提供了页面、中文字体、中文字号、页码、页眉页脚、目录、章节标题样式、章节标号等设置选项。并且提供了封面、图片、表格、引入字体，引入文件、插入代码片等样例。

main.tex使用\documentclass{ctexart}作为文档类别的属性，这是Chinese Tex Article的缩写，是一个现成的模板，目录、摘要等关键词的默认语言就是中文。

main.tex的编译结果就是main.pdf，你可以先看看自己对这个结果是否满意。

#### 2、字体文件夹

目录名：fonts

你自己的字体文件直接放在根目录下就可以了，在导言区设置以下命令：

中文字体：\setCJKmainfont[Path=fonts/,BoldFont=simhei.ttf,ItalicFont=simkai.ttf]{simsun.ttc}

中文字体涵盖黑体、宋体、楷体、仿宋

英文字体：\setmainfont[Path=fonts/]{Times New Roman.ttf}
​                   \setmonofont[Path=fonts/]{Courier New.tff}

这样设置中文字体后，

文本默认的字体是宋体，若调用黑体：\textbf{黑体写在这里}，调用楷体：\textit{楷体写在这里}，调用仿宋：\texttt{仿宋写在这里}。



#### 3、图片文件夹

目录名：include_picture

将所需图片放入该目录下，按如下方式使用：

\includegraphics[scale=0.4]{include_picture/picture.jpg}

#### 4、引用文章文件夹

目录名：include_tex

将需要引用的.tex文件放入该目录下，注意引用的tex只保留文章内容，不需要导言区以及各种格式设置选项，设置格式请在main.tex中完成，样例可参照在include_tex下的include_section.tex文件。

\input{include_tex/include_text} %使用input将在原位置显示

\include{includetex} %使用include将另起一页显示



### 作者的一点期许：

1、希望这个模板能对你有帮助，作为使用或者学习的好素材。

2、希望你在使用时保留main.tex的这些注释：

%Welcome! This is Someday's XeLaTeX Template. 
%Developer: Someday（Yihang Yin,BUAA-SCSE）
%Any advice? Please contact: somedayjiayi@163.com

尊重Someday的著作权，Someday就开放使用权，如果它真的对你起了很大的帮助，可以在见到我的时候请我喝咖啡。

3、记住，官方的说明文档（Documentation）永远是最好的教程。



### 后记：

为什么网上流传的LaTeX模板很多，而我还是要“重新发明轮子”，这是因为，网上绝大多数模板缺少必要的说明，除非你理解每行代码的含义，否则还是无法使用。或者有的模板过于完备或者繁杂，这为通常任务很急的论文写作带来了不小的麻烦，而且我希望自己能慢慢成长为一个LaTeX高手，所以，我自己摸索开发了一个模板。想享受LaTeX带来的便利，直接使用这个模板就好了，但如果你想真正领悟其中的含义，那就自己再发明一次轮子吧!~

