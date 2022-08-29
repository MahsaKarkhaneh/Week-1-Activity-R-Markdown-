# Week-1-Activity-R-Markdown-
---
title: "Diamond sizes"
author: "Mahsa Karkhaneh"
date: "2021"
output:
  word_document: default
  pdf_document: default
---

``` {r, echo = FALSE}
```

```{r setup, include = FALSE}
library(ggplot2)
library(dplyr)
```

```{r, include = FALSE}
smaller <- diamonds %>% 
  filter(carat <= 2.5)
```

```{r, echo = FALSE}
```

We have data about `r nrow(diamonds)` diamonds. Only 
`r nrow(diamonds) - nrow(smaller)` are larger than
2.5 carats. The distribution of the remainder is shown
below:

``` {r, echo = FALSE}
```

```{r, echo = FALSE}
smaller %>% 
  ggplot(aes(carat)) + 
  geom_freqpoly(binwidth = 0.01)
```

```{r, echo = FALSE}
```
[markdown code.txt](https://github.com/MahsaKarkhaneh/Week-1-Activity-R-Markdown-/files/9440808/markdown.code.txt)
[Anna-Sample-Markdown.docx](https://github.com/MahsaKarkhaneh/Week-1-Activity-R-Markdown-/files/9440809/Anna-Sample-Markdown.docx)






