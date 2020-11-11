## 首页不要页码 
1. 在begin命令或者newpage命令之后，马上调用pagenumbering{gobble}，这个可以消掉该页页码
2. 然后在下一页（通常是newpage命令之后），调用pagenumbering{arabic}，重新开始显示页码

## 中文不能显示或者各种错误
1. 直接切换compiler到XeLaTex
2. \usepackage{xeCJK}

## 日语不能显示
1. \usepackage{xeCJK}
2. \setCJKmainfont{IPAMincho}
3. \setCJKsansfont{IPAGothic}
4. \setCJKmonofont{IPAGothic}

## 横屏
1. \usepackage[landscape]{geometry}

## 2列排版，a4纸张大小
1. \documentclass[twocolumn,a4paper]{article}

## 插入图片
1. \usepackage{graphicx}
2. 插入图片如下：
```tex
\begin{figure}
  \includegraphics[]{imgs/01.png}
  \caption{仮想のゴールド要約は、文書とのユークリッド距離は一番近い}
  \label{fig:img1}
\end{figure}
```

## 插入表格
```tex
\begin{table}[]
    \begin{tabular}{|c|}
    \hline
        分割前： ddddddddd \\
        分割後：dd dd dd\\
    \hline
    \end{tabular}
    \caption{}
    \label{tab:my_label}
\end{table}
```

## 表格固定位置
首先在开头加两句，然后在table加H选项
```tex
\usepackage{float}
\restylefloat{table}

...

\begin{table}[H]
```

## 表格加边框
用`|c|`来左右加边框，用`\hline`来上下加边框

```tex
    \begin{tabular}{|c|}
    \hline
        分割前： ddddddddd \\
        分割後：dd dd dd\\
    \hline
    \end{tabular}
```

## 插入引用
首先引用包复制即可，然后声明路径为qhe.bib
```tex
\usepackage[
backend=biber,
style=alphabetic,
sorting=ynt
]{biblatex}

\addbibresource{qhe.bib}
```

qhe文件的内容
```tex
@inproceedings{vinyals2015pointer,
  title={Pointer networks},
  author={Vinyals, Oriol and Fortunato, Meire and Jaitly, Navdeep},
  booktitle={Advances in neural information processing systems},
  pages={2692--2700},
  year={2015}
}

@article{zhong2020extractive,
  title={Extractive Summarization as Text Matching},
  author={Zhong, Ming and Liu, Pengfei and Chen, Yiran and Wang, Danqing and Qiu, Xipeng and Huang, Xuanjing},
  journal={arXiv preprint arXiv:2004.08795},
  year={2020}
}
```
从谷歌复制即可
