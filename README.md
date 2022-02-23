# Vegan and Vegetarian Restaurant Model

**Authors:** Jorit Studer and Larissa Eisele

**Module:** R-Bootcamp (February 25th, 2022)

**Supervisor:** Matteo Tanadini and Claude Renaux

## Project Structure

```
|--analysis.pdf       # Report rendered by Bookdown with static ggWordCloud
|--data\              # Data for the analysis (CSV and XLSX)
|--latex\             # Custom Title Page in Latex
|--references\        # References
  |--references.bib     # BibTeX references
  |--apa.csl            # APA 7th Edition Citation Style Language

|--analysis.html      # Report rendered by Bookdown with animated worcloud2
```

## Installation

The following packages are required to knitr this report using bookdown.

```r
packages <- c("dplyr","readxl", "curl", "ggplot2", "ggrepel", "maps", "stringr", "tm", "wordcloud2", "tidyverse", "RColorBrewer", "ggwordcloud", "viridis", "bookdown", "utils")
package.check <- lapply(packages, FUN = function(x) {
    if (!require(x, character.only = TRUE)) {
        install.packages(x, dependencies = TRUE)
        library(x, character.only = TRUE)
    }
})
```

## Rendering

In R-Studio click on the arrow on Knit then select "Knit to pdf_document2" or "Knit to pdf_html2". 
*The following project was compiled using RStudio 2021.09.2 Build 382 and R version 4.1.2 (2021-11-01).*

## Remarks

The chapter of choice for this paper are Maps, WordClouds and Bookdown.

An animated version of WordCloud about vegan and vegitarian cuisines can only be found in the html version, as it is based on wordcloud2, while the pdf version uses ggwordcloud.