---
title: "Nutrition Indicators"
categories: ["R"]
tags: ["wiki"]
weight: 5
---


The `anthro` package can be used to compute many values relevant to the nutrition survey.

```R
install.packages("anthro", repos = "https://cloud.r-project.org")

# this produces a stratified analysis and includes many indicators that can be used directly in the report
# the meaning of the columns is described here: ?anthro_prevalence
View(
  anthro_prevalence(sex = c(1, 2, 2, 1),
                    age = c(1001, 1000, 1010, 1000),
                    weight = c(18, 15, 10, 15),
                    lenhei = c(100, 80, 100, 100))
)

# for individual z-score calculation you can use this function
anthro_zscores(sex = c(1, 2, 2, 1),
               age = c(1001, 1000, 1010, 1000),
               weight = c(18, 15, 10, 15),
               lenhei = c(100, 80, 100, 100))

```