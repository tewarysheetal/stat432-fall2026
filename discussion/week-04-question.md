---
id: w04-stewary2-lasso-exact-zero
title: "Why does lasso hit exact zero, unlike ridge?"
author: "Sheetal Tewary (stewary2)"
---

For the one-variable lasso problem, the solution is given by soft-thresholding the least-squares estimate:

$$\hat{\beta} = \text{sign}(\hat{\beta}_{LS}) \cdot \max(|\hat{\beta}_{LS}| - \lambda, 0)$$

If $\hat{\beta}_{LS} = 0.8$, sketch how $\hat{\beta}$ changes as $\lambda$ increases from 0 to 1. At what value of $\lambda$ does $\hat{\beta}$ first become exactly zero, and why does the lasso (unlike ridge) hit exactly zero rather than just shrinking toward it?
