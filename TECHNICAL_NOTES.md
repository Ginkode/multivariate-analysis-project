# Technical notes

These notes document small methodological corrections identified while reviewing the original university project for a public portfolio. The submitted R Markdown is intentionally preserved as the coursework artifact.

## Hierarchical clustering: keep full distance precision

The original R Markdown contains:

```r
d <- dist(Z)
d <- round(d, 2)
```

and then passes `d` to `hclust()`.

For a rerun, use the unrounded distance object for clustering:

```r
d <- dist(Z)
hc_s <- hclust(d, method = "single")
hc_c <- hclust(d, method = "complete")
hc_a <- hclust(d, method = "average")
```

If rounded distances are useful for printing or inspection, create a separate display object instead:

```r
d_display <- round(as.matrix(d), 2)
```

This preserves the original precision used by the clustering algorithm.

## Number of clusters

The report explores both `k = 4` and `k = 5`, and the final visualization uses four clusters with complete linkage. In a future rerun, the choice of `k` should also be supported by a quantitative diagnostic such as average silhouette width, rather than relying only on dendrogram and fusion-height inspection.
