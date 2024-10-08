# 文档翻译
* * *

# 前言

此文档的 tex 源码，从这个地址下载 
https://arxiv.org/abs/1812.01537

# 生成英文原文
英文文档默认引擎是 pdflatex。

## 生成原始 pdf 文件
执行2次:
```
$ pdflatex micro_Lie_theory.tex
$ pdflatex micro_Lie_theory.tex
```

第一次生成 pdf 文件。第二次从 micro_Lie_theory.bbl 文件中给 pdf 文件加入索引。

不需要执行 bibtex micro_Lie_theory 命令，因为作者已经提供 micro_Lie_theory.bbl 文件。并且因为没有作者的完整环境，也不能生成该索引文件。

# 更换中文引擎
英文引擎 pdflatex 不能处理中文。中文要换成 xelatex 引擎。

```
在 micro_Lie_theory.tex 文件头部增加一行
%!TEX TS-program = xelatex

line 1: 将
\pdfoutput=1
注释为
%\pdfoutput=1

line 11: 在 "\documentclass{IEEEtran}" 增加一行
\usepackage{ctex}
以便能处理中文

line 154: 将 "pdftex" 变为 "xetex"。 
\usepackage[xetex]{hyperref}

同样要执行两次：

$ xelatex micro_Lie_theory.tex
$ xelatex micro_Lie_theory.tex
```

编译完成后，用 xelatex 生成的 PDF 文件的页数总是比 pdflatex 的要大几页。不知何故，也许和两者的字间距和行间距有关。

# 翻译

接着分别针对每个 tex 文件进行翻译。

这教材里面的数学内容太专业、太高深。在这其中也不知道引入了多少个错误:-(。

读者如有发现错误，请给予指正。谢谢！

