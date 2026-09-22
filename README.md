# Latex

python解释器的位置：
```latex
"E:\APP\Anaconda\python.exe"
```

## Latex代码
### 对字体进行颜色变换：

```latex
\textcolor{red}{对本文中的模型给出比较客观的评价，必须实事求是，有根据，以便评卷人参考。}
```

### 加自动排序123：

```latex
\begin{enumerate}[label=\arabic*、]
	\item 对本文中的模型给出比较客观的评价，必须实事求是，有根据，以便评卷人参考。
	\item 推广和优化，需要花费功夫想出合理的、甚至可以合理改变题目给出的条件的、不一定可行但是具有一定想象空间的准理想的方法、模型。由此做出一些改进方向，也可以是参赛者一些来不及实现的思路。
\end{enumerate}
```

### 给某一段字体更改字体号数：
```latex
{\songti\zihao{-4}本人郑重声明：所提交的毕业论文（设计）。}
```
### 注释
```latex
\begin{rmk}
字数300$\sim $600之间，需控制在一页；摘要中必须将具体方法、模型和所得结果写出来；
\end{rmk}
```
### 开头的点：
```latex
\begin{itemize}

\item 对本文中的模型给出比较客观的评价，必须实事求是，有根据，以便评卷人参考。

\item 推广和优化，需要花费功夫想出合理的、甚至可以合理改变题目给出的条件的、不一定可行但是具有一定想象空间的准理想的方法、模型。
\end{itemize}
```
### 首行缩进: 
```latex
\noindent
```
### 从此处开始取消首行缩进:
```latex
\setlength{\parindent}{0pt}
```

把公式和图片序号改成2.1、2.1
原文:
```latex
\renewcommand\thesection{\arabic{section}}
\renewcommand\thesubsection{\arabic{section}\thinspace.\thinspace\arabic{subsection}}
\renewcommand\thesubsubsection{\thesubsection\thinspace.\thinspace\arabic{subsubsection}}
```
改成：
```latex
\renewcommand\thesection{\arabic{section}}
\renewcommand\thesubsection{\arabic{section}\thinspace.\thinspace\arabic{subsection}}
\renewcommand\thesubsubsection{\thesubsection\thinspace.\thinspace\arabic{subsubsection}}

\numberwithin{equation}{section}
\numberwithin{figure}{section}
\numberwithin{table}{section}
或者：
% 公式、图片和表格按一级标题分章节编号
\numberwithin{equation}{section}
\numberwithin{figure}{section}
\numberwithin{table}{section}

% 强制使用阿拉伯数字，避免受到一级标题中文编号的影响
\renewcommand{\theequation}{\arabic{section}.\arabic{equation}}
\renewcommand{\thefigure}{\arabic{section}.\arabic{figure}}
\renewcommand{\thetable}{\arabic{section}.\arabic{table}}
```
把一级标题是阿拉伯数字改为中文的数字;原文为：
```latex
% 节标题格式, 居中, 使用\chinese命令修改计数器, \kern 使得数字和内容不至于太远
\renewcommand\thesection{\arabic{section}.}
\renewcommand\thesubsection{\arabic{section}\thinspace.\thinspace\arabic{subsection}}
\renewcommand\thesubsubsection{\thesubsection\thinspace.\thinspace\arabic{subsubsection}}
```
改为：
```latex
\renewcommand\thesection{\chinese{section}、}
```











