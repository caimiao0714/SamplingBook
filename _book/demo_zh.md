--- 
title: "title"
author: "author"
date: "2019-04-02"
output:
  bookdown::pdf_book:
    keep_tex: yes
    dev: "cairo_pdf"
    latex_engine: xelatex
    citation_package: natbib
    template: tex/template_yihui_zh.tex
    pandoc_args:  --top-level-division=chapter
    toc_depth: 3
    toc_unnumbered: no
    toc_appendix: yes
    quote_footer: ["\\begin{flushright}", "\\end{flushright}"]
documentclass: ctexbook
bibliography: [bib/bib.bib]
biblio-style: apalike
link-citations: yes
colorlinks: no
lot: yes
lof: yes
geometry: [b5paper, tmargin=2.5cm, bmargin=2.5cm, lmargin=3.5cm, rmargin=2.5cm]
site: bookdown::bookdown_site
description: "一个简单的中文书示例。"
github-repo: yihui/bookdown-chinese
#cover-image: images/cover.jpg
---

　　

\mainmatter

<!--chapter:end:index.Rmd-->


# 前言 {-}

你好，世界。我写了一本书。这本书是这样的，第 \@ref(intro) 章介绍了啥啥，然后是啥啥……

我用了两个 R 包编译这本书，分别是 **knitr**\index{knitr} [@xie2015] 和 **bookdown**\index{bookdown} [@R-bookdown]。以下是我的 R 进程信息：


```r
sessionInfo()
```

```
## R version 3.5.3 (2019-03-11)
## Platform: x86_64-w64-mingw32/x64 (64-bit)
## Running under: Windows 10 x64 (build 16299)
## 
## Matrix products: default
## 
## locale:
## [1] LC_COLLATE=English_United States.1252 
## [2] LC_CTYPE=English_United States.1252   
## [3] LC_MONETARY=English_United States.1252
## [4] LC_NUMERIC=C                          
## [5] LC_TIME=English_United States.1252    
## 
## attached base packages:
## [1] stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
## [1] bookdownplus_1.5.6 bookdown_0.9      
## 
## loaded via a namespace (and not attached):
##  [1] Rcpp_1.0.0       packrat_0.5.0    digest_0.6.18    pacman_0.5.1    
##  [5] magrittr_1.5     evaluate_0.13    xaringan_0.9     stringi_1.4.3   
##  [9] rstudioapi_0.9.0 magick_2.0       rmarkdown_1.12   tools_3.5.3     
## [13] stringr_1.4.0    tinytex_0.11     xfun_0.5         yaml_2.2.0      
## [17] compiler_3.5.3   htmltools_0.3.6  knitr_1.22
```

## 致谢 {-}

非常感谢谁谁以及谁谁对我的帮助。艾玛，要不是他们神一样的队友，我两年前就写完这本书了。

\BeginKnitrBlock{flushright}<p class="flushright">张三  
于 A 村某角落</p>\EndKnitrBlock{flushright}

# 作者简介 {#author .unnumbered}

上不了厅堂，下得了厨房。敲得了代码，逮得住蟑螂。

`\mainmatter`

# 牛刀小试 {#intro}

现在我们可以试试 **bookdown** 的一些初级功能了，例如图表。图 \@ref(fig:hello) 是一幅无趣的散点图，表 \@ref(tab:iris) 是一份枯燥的数据。


```r
par(mar = c(4, 4, 1, .1))
plot(cars, pch = 19)
```

\begin{figure}
\includegraphics[width=0.9\linewidth]{demo_zh_files/figure-latex/hello-1} \caption{<U+96F7><U+7334><U+554A>,<U+6563><U+70B9><U+56FE>!}(\#fig:hello)
\end{figure}


```r
knitr::kable(
  head(iris), caption = '雷猴啊，iris 数据！',
  booktabs = TRUE
)
```

\begin{table}[t]

\caption{(\#tab:iris)<U+96F7><U+7334><U+554A>,iris <U+6570><U+636E>!}
\centering
\begin{tabular}{rrrrl}
\toprule
Sepal.Length & Sepal.Width & Petal.Length & Petal.Width & Species\\
\midrule
5.1 & 3.5 & 1.4 & 0.2 & setosa\\
4.9 & 3.0 & 1.4 & 0.2 & setosa\\
4.7 & 3.2 & 1.3 & 0.2 & setosa\\
4.6 & 3.1 & 1.5 & 0.2 & setosa\\
5.0 & 3.6 & 1.4 & 0.2 & setosa\\
\addlinespace
5.4 & 3.9 & 1.7 & 0.4 & setosa\\
\bottomrule
\end{tabular}
\end{table}

就这样，你可以一直编下去，直到编不下去。

\cleardoublepage 

# (APPENDIX) 附录 {-}

# 余音绕梁 {#sound}

呐，到这里朕的书差不多写完了，但还有几句话要交待，所以开个附录，再啰嗦几句，各位客官稍安勿躁、扶稳坐好。



<!--chapter:end:body.Rmd-->

