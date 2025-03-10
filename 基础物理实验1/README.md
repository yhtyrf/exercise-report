# SYSU-SPA-Labreport-Template
**中山大学物理与天文学院本科实验报告LaTeX模板**
<p align = "center">
<img src="https://github.com/Huanyu-Shi/SYSU-SPA-Labreport-Template/blob/main/images/example.png" width="20%" />
<p>

大家好，我是来自于物理与天文学院2019级物理系的本科生Huanyu Shi。

本模板源于我大二时期一时兴起所做。对于撰写实验报告，学院只提供了简陋的word模板，使用word效率低下且排版效果不甚理想。于是我仿照学院提供的模板格式，在其基础上完成了此 $\LaTeX$ 模板。

临近毕业，我发现此模板在学院内部仍有流传，但毕竟当时写就并不规范，且功能有诸多缺失。考虑到种种原因，**我决定将此模板进行更新完善并打包公布在Github和知乎上**，希望有助于后辈学子，同时也希望对其他兄弟院校的同学有一定参考和帮助作用。

同时，也欢迎访问我的[知乎个人主页](https://www.zhihu.com/people/za-ran-zhu-fu-liu-xing)

# 模板功能说明
本模板经过更新完善后，除几个必要的实验报告部分：
* 扉页
* 预习报告
* 实验记录
* 分析与讨论

在此前的实验报告基础上我增加了以下几个内容：
* **参考文献**，注明引用内容是是作者对他人知识成果的承认和尊重，是保证学术诚信必需养成的习惯，不可缺失：

<img src="https://github.com/Huanyu-Shi/SYSU-SPA-Labreport-Template/blob/main/images/readme1.JPG" width="60%" />

* **代码附录**，给出了使用Lstlisting环境展示实验报告中所用代码的示例：
<img src="https://github.com/Huanyu-Shi/SYSU-SPA-Labreport-Template/blob/main/images/readme2.JPG" width="60%" />

* **常用命令展示**，鉴于部分学生初次接触 $\LaTeX$，本模板也给出了相应的常用命令展示以方便查阅。
<img src="https://github.com/Huanyu-Shi/SYSU-SPA-Labreport-Template/blob/main/images/readme3.JPG" width="60%" />

<img src="https://github.com/Huanyu-Shi/SYSU-SPA-Labreport-Template/blob/main/images/readme4.JPG" width="60%" />

<img src="https://github.com/Huanyu-Shi/SYSU-SPA-Labreport-Template/blob/main/images/readme5.JPG" width="60%" />

# 一些注意事项
1. 参考文献应导入`bib`文件中，编译顺序请按`xelatex`->`bibtex`->`xelatex`->`xelatex`；
2. `lstlisting`代码环境配置如下，可更改为其他语言，其他相关配置可参考`listings`宏包的手册，
```latex
\usepackage{listings}

\definecolor{c1}{HTML}{2752C9} % 定义的颜色
\lstloadlanguages{python}

\lstdefinestyle{pythonstyle}{
backgroundcolor=\color{gray!5},
language=python,
frameround=tftt,
frame=shadowbox, 
keepspaces=true,
breaklines,
columns=spaceflexible,                   
basicstyle=\ttfamily\small, % 基本文本设置，字体为teletype，大小为scriptsize
keywordstyle=[1]\color{c1}\bfseries, 
keywordstyle=[2]\color{Red!70!black},   
stringstyle=\color{Purple},       
showstringspaces=false,
commentstyle=\ttfamily\scriptsize\color{green!40!black},% 注释文本设置，字体为sf，大小为smaller
tabsize=2,
morekeywords={as},
morekeywords=[2]{np, plt, sp},
numbers=left, % 代码行数
numberstyle=\it\tiny\color{gray}, % 代码行数的数字字体设置
stepnumber=1,
rulesepcolor=\color{gray!30!white}
}
```
3. 本模板定义了两种形式的`box`，可参考`tcolorbox`宏包的手册进行修改，
```latex
\usepackage{tcolorbox}
\tcbuselibrary{skins,breakable}
\newtcolorbox{tbox}[2][]{
  colframe=black!70!,
  breakable,
  enhanced,
	boxrule =0.5pt,
  title = {#2},
  fonttitle = \large\kaishu\bfseries,
	drop fuzzy shadow,
  #1
}
\newtcolorbox[auto counter,number within=section]{question}[1][]{
  top=2pt,bottom=2pt,arc=1mm,
  boxrule=0.5pt,
  breakable,
  enhanced,
  coltitle=c1!80!gray,
  colframe=c1,
  colback=c1!3!white,
  drop fuzzy shadow,
  title={思考题~\thetcbcounter：\quad},
  fonttitle=\bfseries,
  attach title to upper,
  #1
}
```
<img src="https://github.com/Huanyu-Shi/SYSU-SPA-Labreport-Template/blob/main/images/readme6.JPG" width="60%" />

# 声明
* 本模板仅供学习交流所用，非学院官方模板。
* 本模板不再进行更新维护，若有任何额外需求请自行设计更改。

