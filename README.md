# Someday's XeLaTeX Template

## Someday的XeLaTeX中文模板

首先，如果你是初学者，不要一进来就发现是XeLaTeX而不是LaTeX，然后就匆匆离开。XeLaTeX本身就是LaTeX的一个分支，很多命令可以通用，XeLaTeX的优点是支持第三方字体。

现在，欢迎你使用Someday出品的TeX模板，因为网上很多模板下载下来根本无法使用，而且最最让人头痛的就是LaTeX对中文的支持很不友好，所以我采用了XeLaTeX，因为可以导入第三方字体。然后我从头学习，从配置到尝试，自己搭建了一个模板，希望对你有帮助！

该模板首次发布于微信公众平台“SomedayWill”，在使用模板的过程中有任何问题、任何的Bug及改进意见，欢迎关注微信公众平台“SomedayWill”，并在后台提问，后台君就是Someday本人。

![SomedayWill_QR_code](SomedayWill_QR_code.jpg)



### 可选编译方式：

####1、Sublime Text：

Someday使用的是Mac系统，Sublime Text2用Package Control安装Latextool插件后进行编译，编译模式为XeLaTeX，可以直接编译。

####2、在线TeX IDE：

在www.sharelatex.com网站上也可以直接编译，编译选项为XeLaTeX。

####3、命令行编译：

在TeXLive2016环境下，编译命令如下：

cd  <模板根目录> 
xelatex main.tex 

#### 4、本地IDE编译：

本机已经安装TeX套装、TeX IDE等亦可编译，注意编译选项为XeLaTeX即可。



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
%Developer: Someday（BUAA-SCSE）
%任何问题或建议，欢迎关注微信公众平台“SomedayWill”，并在后台提问~



尊重Someday的著作权，Someday就开放使用权，如果它真的对你起了很大的帮助，可以在见到我的时候请我喝咖啡。

3、记住，官方的说明文档（Documentation）永远是最好的教程。



### 后记：

为什么网上流传的LaTeX模板很多，而我还是要“重新发明轮子”，这是因为，网上绝大多数模板缺少必要的说明，除非你理解每行代码的含义，否则还是无法使用。或者有的模板过于完备或者繁杂，这为通常任务很急的论文写作带来了不小的麻烦，而且我希望自己能慢慢成长为一个LaTeX高手，所以，我自己摸索开发了一个模板。想享受LaTeX带来的便利，直接使用这个模板就好了，但如果你想真正领悟其中的含义，那就自己再发明一次轮子吧!~



### 注意：如果你是我航学子，并因冯如杯使用该模板

该模板目前满足了冯如杯论文的如下要求：

1、字体字号

​	论文题目:二号,华文中宋体加粗,居中。
​	章标题:三号,黑体,居中。
​	节标题:四号,黑体,居左。
​	正文:小四号,中文字体为宋体,西文字体为 Times New Roman 体,首行缩进,两端对齐。		  

​	页码:五号宋体数字和字母,Times New Roman 体。

2、页边距

​	上边距:25mm;下边距:25mm;左边距:30mm;右边距 20mm。

3、页眉

​	页眉用小五号宋体字，居中，页眉标注从论文主体部分开始(绪论或第一章)。

​	格式已经符合，请自行修改内容。

4、页码

​	页码从主体部分开始用五号阿拉伯数字连续编码,页码位于页脚居中。封面、题名页不编页码。

​	摘要、目录、图标清单、主要符号表用五号小罗马数字连续编码,页码位于页脚居中。

5、封面

​	样式基本符合，图的位置已经按照word模板中的空行设置。

6、目录

​	我航对目录其实没有格式上的要求，可以放松心使用。



其它要求，请等待作者不断更新，未完待续。



### UPDATE 2017.07.14

1、增加LaTeX符号对应表----LaTeX simbols table.pdf

2、增加了“注意：如果你是我航学子，并因冯如杯使用该模板”说明



###UPDATE 2017.09.08

经123学长指正，Someday于2017.09.08进行一次重要更新，内容包括：

1、对中文字号的设置命令进行了修改，使用方法不变。

2、对仿宋字体所在的fontstyle进行了修改，以适应fontspec宏包。

3、将取消首页页码的命令改为：pagenumbering{gobble} 

以上修正解决了以前版本中编译报错问题，当前版本在TeXLive2016环境下已经可以一次编译成功。 

编译命令如下： 

cd  <模板根目录> 

xelatex main.tex 





