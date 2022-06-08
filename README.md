# PKU_SMS_UG_Thesis
A $\LaTeX$ implementation of the PKU thesis template in 2022. It consists of one style file `pkuugthesis.sty` and two vector images (the logo `pkulogo.eps` and the name `pkuword.eps`).
The TeX code heavily depends on the projects [Bochen Tan (2019)](https://github.com/tbcdebug/PKU_EECS_UGR_THSS) and [Casper Ti. Vector (2017)]( https://github.com/JoeHF/aet_paper). Gratitudes to these amazing people.

这是2022年PKU本科毕业论文的一种$\LaTeX$实现，主要组成部分为样式文件`pkuugthesis.sty`和两张图片 (`pkulogo.eps`、`pkuword.eps`)。
本项目受到[Bochen Tan (2019)](https://github.com/tbcdebug/PKU_EECS_UGR_THSS)和[Casper Ti. Vector (2017)]( https://github.com/JoeHF/aet_paper)的重大影响。感谢他们。

## Usage of the style file
The style file only provides the typesetting of the cover page.
I use brute force such as `\vspace`, `\hspace`, `\makebox[width]` and `\parbox[position][height]{width}{text}` to set the spacings in the template, which was provided as a MS Word document. You may adjust the lengths to your own needs.

You must set `documentclass` to `ctexbook` in order to use this style file.

The font names (see comments in `pkuugthesis.sty`) may also need to be changed for different system requirements (I use macOS Big Sur 11.5).

## :bangbang: Further operations besides the style file :bangbang:
You should also input the following commands **AFTER** `\begin{document}` to set the headers and footers (use the package `fancyhdr` first).
```LaTeX
% get title
\makeatletter
\let\Title\@title
\makeatother
\setlength{\headheight}{13pt}
\fancypagestyle{pkuthesis}{
    \ctexset{chapter/pagestyle=pkuthesis}
    \fancyhead[L,R]{}
    \fancyhead[C]{\Title}
    \fancyfoot[C]{第 \thepage 页}
}
```
Also, you should add this line of command at the beginning of the first chapter. This changes the header and footer styles of the main text.
```LaTeX
\pagestyle{pkuthesis}
```

Have fun! :unicorn:
