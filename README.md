# HW-3
---
title: "[HW3 Data Wrangling]"
description: |
  
  
  In this distill blog post I will be reading in the eggs data and perforrming basic data wrangling operations using dplyr functions.
Your Name: Tyler Paske
date: 09-26-2021
output:  
  distill::distill_article:
    self_contained: false
draft: true
---
[Eggs Data]

A tibble: 120 x 6
   month      year large_half_dozen large_dozen extra_large_half_dozen extra_large_dozen
   <chr>     <dbl>            <dbl>       <dbl>                  <dbl>             <dbl>
 1 January    2004             126         230                    132               230 
 2 February   2004             128.        226.                   134.              230 
 3 March      2004             131         225                    137               230 
 4 April      2004             131         225                    137               234.
 5 May        2004             131         225                    137               236 
 6 June       2004             134.        231.                   137               241 
 7 July       2004             134.        234.                   137               241 
 8 August     2004             134.        234.                   137               241 
 9 September  2004             130.        234.                   136.              241 
10 October    2004             128.        234.                   136.              241 
#... with 110 more rows

[Rows: 120 Columns: 6]

******************************Manipulating the Data with dplyr**************************

(((SELECT))) "Retrieving the data we want to use"

A tibble: 120 x 2
    year extra_large_dozen
   <dbl>             <dbl>
 1  2004              230 
 2  2004              230 
 3  2004              230 
 4  2004              234.
 5  2004              236 
 6  2004              241 
 7  2004              241 
 8  2004              241 
 9  2004              241 
10  2004              241 
# ... with 110 more rows

(((FILTER))) "Filtering the year wanted, 2004"

A tibble: 12 x 1
   extra_large_dozen
               <dbl>
 1              230 
 2              230 
 3              230 
 4              234.
 5              236 
 6              241 
 7              241 
 8              241 
 9              241 
10              241 
11              241 
12              241 

(((ARRANGE))) "Arranging the data from largest to smallest"

A tibble: 12 x 1
   extra_large_dozen
               <dbl>
 1              241 
 2              241 
 3              241 
 4              241 
 5              241 
 6              241 
 7              241 
 8              236 
 9              234.
10              230 
11              230 
12              230 


(((SUMMARISE))) "Getting an understanding of what the smallest output was in 2004"

A tibble: 1 x 1
  XLEggs_2004 =
        <dbl>
            230

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = FALSE)
```

Distill is a publication format for scientific and technical writing, native to the web.

Learn more about using Distill at <https://rstudio.github.io/distill>.
