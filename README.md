# SRM611-student-absence
# Weekend Alcohol Use and School Absences

## Purpose
This repository contains the count regression analysis of SRM 611 (Project 3).
It examines the association between alcohol use on weekends and the number of school absences among secondary school students, controlling for study time, previous class failures, sex, age and school. First, a Poisson model is fitted, tested for overdispersion, and compared with a negative binomial model.

## Data Source 
Student Performance data set (Portuguese language course, 649 students), from UCI Machine Learning Repository, downloaded from Kaggle:
https://www.kaggle.com/datasets/uciml/student-alcohol-consumption

The data used are public and non-identifiable.

## Files 
| File | Description | |---|---| | `Project3.Rmd` | R Markdown file with full analysis: data exploration, Poisson and negative binomial models, model comparison and diagnostics | | `student-por.csv` | Data file (649 students, 33 variables) | | `README.md` | This file |

## How to Replicate
1. Clone or download this repo.
2. Open ‘Project3.Rmd’ with RStudio. Put it in the same folder as student-por.csv.
3. Install necessary packages if needed: `install.packages(c("ggplot2", "knitr", "MASS"))`
4 Click **Knit**.

## The main result
The Poisson model was severely overdispersed (Pearson X²/df = 4.93), so a negative
binomial model was recommended. Each one-level increase in weekend alcohol use was
associated with about 16% more expected absences (IRR = 1.16, 95% CI 1.07–1.27).
