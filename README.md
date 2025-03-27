# RNA-seq Analysis for FAP Duodenal Tissue Study

This repository contains the full RNA-seq analysis pipeline used in the study:

**"IL-17A-producing NKp44⁻ group 3 innate lymphoid cells accumulate in Familial Adenomatous Polyposis duodenal tissue"**  
_Kaiser et al., 2024_

## Overview

This pipeline performs differential expression analysis and visualization using bulk RNA-seq data from FAP patient duodenal tissue. It includes setup, normalization, PCA, DEG identification, and plotting (volcano plots and heatmaps).

The analysis is based on [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html) and customized ggplot-based visualizations.

## Features

- Installation and loading of required CRAN and Bioconductor packages
- Project-specific metadata handling and directory setup
- PCA of normalized gene expression data
- Differential gene expression (DEG) analysis between user-defined groups
- Volcano plot generation
- ComplexHeatmap visualizations



## Requirements

- R ≥ 4.0.3
- DESeq2
- ggplot2, patchwork, ggrepel, ComplexHeatmap
- clusterProfiler, org.Hs.eg.db
- Kallisto or STAR count matrix
- MultiQC outputs (optional but recommended)

Install packages manually install them as outlined in the first section of the `.Rmd`.

## Usage

1. Clone this repo:
```bash
git clone https://github.com/yourusername/FAP_duodenum_RNAseq.git
cd FAP_duodenum_RNAseq
```

2. Adjust the project-specific information in the `20211014_DESeq_Github.Rmd` file:
   - Experimental groups
   - Sample IDs and paths
   - Species (e.g., `org.Hs.eg.db` for human)

3. Run the analysis in RStudio by knitting the `.Rmd` file to HTML.

4. Key outputs:
   - Normalized counts and PCA plots
   - DEG tables
   - Volcano plots

## Citation

If you use this code or part of it, please cite:

*Kaiser et al., IL-17A-producing NKp44⁻ group 3 innate lymphoid cells accumulate in Familial Adenomatous Polyposis duodenal tissue, 2024.*

## License

MIT License

---

For questions, contact:  
[benjamin.kraemer@ukbonn.de](mailto:benjamin.kraemer@ukbonn.de)  
[jacob.nattermann@ukbonn.de](mailto:jacob.nattermann@ukbonn.de)
