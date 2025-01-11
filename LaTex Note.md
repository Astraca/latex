# LaTex
## Chapter 0
`LaTeX Workshop`中有多个命令进行构建。它们之间存在一定差异：
> + XeLaTeX: 支持Unicode，适合处理多语言文档；支持使用系统字体
  + PDFLaTeX: 不支持Unicode(需使用特定的包来处理非ASCII字符)，直接生成PDF
  + BibTeX: 处理参考文件；通过`.bib`管理文献条目并生成参考文献列表
  + LaTeXmk: 自动化工具用于编译LaTeX文档；自动检测依赖关系
### 中文
```tex
\documentclass{article}
\usepackage{fontspec}
\usepackage{xeCJK} % 支持中文字体设置和中英文间距调整

% 设置英文字体
\setmainfont{Times New Roman} % 英文字体设置为 Times New Roman
\setsansfont{Arial}           % 无衬线字体设置为 Arial
\setmonofont{Courier New}     % 等宽字体设置为 Courier New

% 设置中文字体
\setCJKmainfont{SimSun}       % 中文正文字体设置为宋体
\setCJKsansfont{SimHei}       % 中文无衬线字体设置为黑体
\setCJKmonofont{FangSong}     % 中文等宽字体设置为仿宋

% 可选：调整中英文间距
\xeCJKsetup{CJKglue=\hskip 0.2em}

\begin{document}

这是中文测试。This is an English test.

\textsf{这是中文无衬线字体。This is English sans-serif.}

\texttt{这是中文等宽字体。This is English monospace.}

\end{document}
```
## Chapter 1. 