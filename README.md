# FRB Template

- [FRB Template](#frb-template)
  - [Notice](#notice)
  - [编译方式](#编译方式)
  - [效果图](#效果图)

## Notice
本项目由Somedaywilldo学长的[项目](https://github.com/Somedaywilldo/Someday-XeLaTex-Template)改进而来。

**本项目将择日开始重构, 主要是大量的`\setCJKxxx`不再是新版本`Ctex`包的推荐选项, ~~以及写基物实验的时候会出现莫名其妙的交叉引用错误~~, 目前不建议使用该模板进行冯如杯等正式作品的写作!!!**


采用本模板的项目已经通过了学院审核以及学校审核. 通过校审的截图如下~

![](include_picture/pass.png)

主要参考了[第三十届“冯如杯”学生创意大赛论文撰写格式规范](Reference/第三十届“冯如杯”学生创意大赛论文撰写格式规范.docx)在保留原License以及作者信息的同时对原来模板的一些细节进行了修改：
- 增加了副标题对华文新魏的支持
- 增加了对外文参考文献无出版地点s:l, s:n的修正，直接复用了[南大学位论文](http://haixing-hu.github.io/nju-thesis/)提供的bst文件
- 重新组织章节分为各个小chap.tex
- 增加了对结语的支持
- 修改了图表标题为宋体加粗
- 改正了标题格式以及目录格式
- 修改了图表标题文字

请注意原repo中的须知仍然有效，请参阅[须知](README_Origin_repo.md)

## 编译方式
Pannenets的环境：
- Ubuntu 18.04.04
- texlive-full
- vscode
- LaTex Workshop
- Recipe: XeLaTex + BibTex + ExLatex * 2

理论上win10可用同样的配置，或者采用WSL(最好的Linux发行版)进行编译


## 效果图

请看[编译结果](FRBKeJi.pdf)