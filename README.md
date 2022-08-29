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



My own MarkDown with HairEyeColor dataframe
---
title: "HairEyeColor"
author: "Mahsa Karkhaneh"
date: '2022-08-29'
output: word_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
library(package="dplyr")
library(ggplot2)
```

## R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

```{r HairEyeColor}
HairEyeColor<- as.data.frame(HairEyeColor)
summary(HairEyeColor)
head(HairEyeColor,1)
HairEyeColor %>%
  group_by(Sex)%>%
  print()
total=mutate(HairEyeColor, total=cumsum(Freq))
total
```
```{r, echo = FALSE}
HairEyeColor %>%
  plot(aes(Sex))
```
[HairEyeColor cod.txt](https://github.com/MahsaKarkhaneh/Week-1-Activity-R-Markdown-/files/9440816/HairEyeColor.cod.txt)
[HairEyeColor-Markdown.docx](https://github.com/MahsaKarkhaneh/Week-1-Activity-R-Markdown-/files/9440817/HairEyeColor-Markdown.docx)


