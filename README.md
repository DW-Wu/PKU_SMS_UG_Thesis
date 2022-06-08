# PKU_SMS_UG_Thesis
A modification of the PKU thesis template in 2022. It consists of one style file `pkuugthesis.sty` and two vector images (the logo `pkulogo.eps` and the name `pkuword.eps`).
The TeX code heavily depends on the projects [Bochen Tan (2019)](https://github.com/tbcdebug/PKU_EECS_UGR_THSS) and [Casper Ti. Vector (2017)]( https://github.com/JoeHF/aet_paper). Gratitudes to these amazing people.

## Usage of the style file
The style file only provides the typesetting of the cover page.
I use brute force such as `\vspace`, `\hspace`, `makebox[width]` and `\parbox[position][height]{width}{text}` to set the spacings in the template, which was provided as a MS Word document. You may adjust the lengths to your own needs.

You must set `documentclass` to `ctexbook` in order to use this style file.

## :bangbang: Further operations besides the style file :bangbang:
You should also input the following commands after `\begin{document}` to set the headers and footers (use the package `fancyhdr` first).
```LaTeX
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
