---
id: w07-stewary2-qda-feature-selection
title: "QDA and Feature Selection"
author: "Sheetal Tewary (stewary2)"
---

In Homework 7, QDA could not be fitted using all 256 pixel predictors because the covariance matrices were singular. Reducing the predictors to 40 resolved this issue, but reducing them further to 10 increased the test misclassification rate.

How can we determine the appropriate number of predictors for QDA so that the covariance matrices remain invertible without losing too much information needed for classification?
