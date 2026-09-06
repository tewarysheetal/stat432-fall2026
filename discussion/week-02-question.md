---
id: w02-stewary2-train-test-mse-tradeoff
title: "Why does test MSE U-shape, not training MSE?"
author: "Sheetal Tewary (stewary2)"
---

In the Week 2 simulation, training MSE always decreases (or stays flat) as more covariates are added, but test MSE follows a U-shape — it improves initially, then gets worse. Since both training and test data come from the same underlying data-generating process, why don't they behave the same way as model complexity increases? Specifically, what is each additional covariate "spending" that helps training fit but doesn't necessarily help prediction on new data?
