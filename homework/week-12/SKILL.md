---
name: unsupervised-clustering
description: >
  Compare multiple clustering algorithms, select a suitable
  method using unsupervised criteria, and produce a concise
  one-page analysis report. Load only when explicitly invoked.
disable-model-invocation: true
---

# Unsupervised Clustering Analysis Skill

## Purpose
Explore clustering structure using multiple algorithms,
select one based on unsupervised evidence, and explain its
results in a clearly readable, one-page report.

## Inputs (Provided at Invocation)
- Dataset path or DataFrame
- Observation identifier (optional)
- Clustering feature columns
- Known class labels (optional; interpretation only)
- Random seed (default: 2026)

Never assume dataset-specific variable names or results.

## 1. Data Preparation
- Report the number of observations and features.
- Check missing values, constant features, and duplicates.
- Exclude identifiers and known class labels from fitting.
- Impute missing values if needed and document the method.
- Standardize features when appropriate.
- Consider PCA for high-dimensional data, selecting the
  number of components using explained variance and
  sample size. Fit preprocessing on the feature data only.
- Apply comparable preprocessing across methods.

## 2. Candidate Clustering Methods
Fit and tune at least three distinct algorithms:

### K-means
- Explore multiple values of k.
- Use multiple random initializations.
- Compare within-cluster variation and silhouette scores.

### Hierarchical Clustering
- Compare linkage methods such as Ward and average.
- Explore multiple cluster cuts.
- Use a distance metric appropriate for the features.

### Spectral Clustering
- Explore multiple values of k.
- Tune the similarity graph or kernel parameters.
- Use multiple random seeds when appropriate.

Additional algorithms may be considered if justified.
PCA, UMAP, and other embeddings are not clustering methods.

## 3. Tuning and Model Selection
- Select a reasonable candidate range of cluster counts,
  considering sample size and cluster interpretability.
- Use silhouette score as a primary separation criterion.
- Assess stability under repeated runs or subsampling.
- Examine cluster sizes and avoid unjustified singleton
  clusters or highly imbalanced partitions.
- Consider computational reliability and sensitivity to
  tuning parameters.
- Compare methods using the same feature representation
  wherever possible.
- Do not select a method solely because it maximizes one
  metric. Explain trade-offs and justify the final choice.
- Use known class labels only after final selection.
  Never use them to tune k, preprocessing, or algorithms.

## 4. Final Clustering Interpretation
For the selected method only:
- Report the chosen algorithm and tuning parameters.
- Report the number and sizes of clusters.
- Describe cluster separation and relevant structure.
- Identify important distinguishing features or patterns,
  using appropriate summaries.
- If known labels are available, compare them with the
  selected clusters only after fitting and selection.
- Treat label agreement as interpretation, not evidence
  used to select the clustering method.
- Explain uncertainty, limitations, and possible
  sensitivity to preprocessing or parameter choices.

## 5. Visualization
- Produce one meaningful visualization of the selected
  clustering, preferably a PCA scatterplot with points
  colored by assigned cluster.
- Label axes and report explained variance when using PCA.
- Use observation identifiers only when readable.
- Optionally include a compact cluster summary table.
- Ensure that colors, labels, and legends remain legible
  at normal printed-page size.
- Do not display clustering results from rejected methods.

## 6. One-Page Analysis Report
**STRICT LIMIT: The generated analysis report must fit
on one printed page, including all text, figures, and tables.**

Include:
1. Brief data description and preprocessing.
2. Algorithms considered and selection criteria.
3. Justification for the selected algorithm.
4. Results from ONLY the selected clustering method.
5. One meaningful figure and/or compact summary table.
6. Interpretation of groups and main limitations.

Other methods may be named briefly to explain selection,
but their clustering results must NOT be presented.

Use concise language, readable fonts, and clear figure
labels. Prioritize substantive findings over decoration.

## 7. Validation and Deliverables
- Verify that fitting and selection exclude known labels.
- Check reproducibility using the supplied random seed.
- Verify that all reported statistics match the analysis.
- Ensure the analysis report occupies no more than one
  printed page.
- Append the complete SKILL.md definition after the
  one-page report as an appendix, outside the page limit.
- Save the report in the requested PDF or HTML format.
- Save this complete skill separately as SKILL.md.
