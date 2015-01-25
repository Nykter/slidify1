---
title       : Data Presentation
subtitle    : Developing data products
author      : Ricardo Merino
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Regression Explorer

As an addition to the regression explorer app in [Shiny App](https://nykter.shinyapps.io/Main/) here is an explanation on how to select the best model.

1. Explore correlation between variables.
2. With package **Leaps** find the model with the smallest residual sum of squares but avoiding overfitting.
3. Or directly plot Mallow's Cp for each model.

--- 

### Correlation

Correlation and dependance between the four variables in the Ozone dataset.

![plot of chunk unnamed-chunk-1](assets/fig/unnamed-chunk-1-1.png) 

---

### Leaps: Find the best model.

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png) 

---

### Mallow's Cp

Mallows's Cp addresses the issue of overfitting, in which model selection statistics such as the residual sum of squares always get smaller as more variables are added to a model. The Cp statistic calculated on a sample of data estimates the mean squared prediction error (MSPE). 

The MSPE will not automatically get smaller as more variables are added. The optimum model under this criterion is a compromise influenced by the sample size, the effect sizes of the different predictors, and the degree of collinearity between them.

![plot of chunk unnamed-chunk-3](assets/fig/unnamed-chunk-3-1.png) 
