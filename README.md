# RNA-Seq Functional Enrichment Analysis: Over-Representation Analysis and Gene Set Enrichment Analysis using Gene Ontology

This tutorial aims to give detailed explanation on how to apply two different methods of functional enrichment, Over-Representation Analysis and Gene Set Enrichment Analysis, to RNA-Seq data using Gene Ontology. Two tutorials are available for the analysis of both bulk RNA-Seq and single-cell RNA-Seq data. 

The data used for illustration of the analysis is taken from: 
- Bulk RNA-Seq: https://doi.org/10.1371/journal.pone.0099625
- Single-cell RNA-Seq: https://doi.org/10.1126/science.aaa1934 

## Table of contents 
- **Data Loading** – Load RNA-seq counts and sample metadata
- **Differential Expression Analysis** – Identify differentially expressed genes
- **Over-Representation Analysis** – Perform ORA using Gene Ontology
- **Gene Set Enrichment Analysis** – Perform GSEA using Gene Ontology
- **Conclusion** – Summary of workflow and recommendations
- **References** – Source datasets and packages

## Installation

### CRAN packages
```r
install.packages(c("tidyverse", "ggplot2", "ggupset", "Seurat"))
```

### Bioconductor packages
```r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install(c(
    "scRNAseq", "clusterProfiler",
    "AnnotationDbi", "org.Mm.eg.db", "enrichplot"
))
```
## Usage 
1. Clone the repository:
```bash
git clone https://github.com/themishalka/Tutorial-GO-enrichment-and-GSEA.git 
```
2. Open the tutorial: Tutorial_scRNAseq.qmd for single-cell or Tutorial_bulkRNAseq.qmd for bulk
3. Render the html to visualise the results:
```r
quarto render Tutorial_scRNAseq.qmd
quarto render Tutorial_bulkRNAseq.qmd
```

