# Bulk RNA-Seq analysis
Project for the Transcriptomic course of "Bioinformatics for Computational Genomics" MSc.

The vignette can be visualized [here](http://htmlpreview.github.io/?https://github.com/ecianini/bulk_RNA-Seq/blob/main/bulk_project.html).

## Aim 
In this work RNA-seq data are analyzed in order to find and characterize differentially expressed (DE) genes. RNA-seq experiments are in fact widely used to understand how RNA-based mechanisms impact gene regulation, and thus disease and phenotypic variation as in tumoral contexts.

## Outline
The RNA-seq data were retrieved from [Recount2](https://jhubiostatistics.shinyapps.io/recount/) as part of the *GTEx project database*.
Three tissues (i.e., liver, heart and colon) with three replicates per tissue were downloaded and provided in normalized/scaled "Ranged Summarized Experiment" format of Recount.

[EdgeR](https://bioconductor.org/packages/release/bioc/html/edgeR.html) was choosen for the analysis of the gene expression data.

The  DE genes call was done performing all the pairwise comparison: 
* Colon vs heart
* Colon vs liver
* Heart vs liver

Starting from the list of DE genes for each tissue we retrieved:
* genes found to be up-(down-)regulated with respect to either one of the other two
* genes found to be up- (down-) regulated with respect to both the other two

As a final step, [EnrichR](https://maayanlab.cloud/Enrichr/), a common functional enrichment analysis tool, was used to determine whether the enriched categories, GO annotations, and pathways were consistent with the up/down regulated genes of the considered tissues.

## References 

Collado-Torres L, Nellore A, Kammers K, Ellis SE, Taub MA, Hansen KD, Jaffe AE, Langmead B, Leek JT. Reproducible RNA-seq analysis using recount2. Nature Biotechnology, 2017. doi: 10.1038/nbt.3838.

Robinson MD, McCarthy DJ, Smyth GK (2010). “edgeR: a Bioconductor package for differential expression analysis of digital gene expression data.” Bioinformatics, 26(1), 139-140.

Chen EY, Tan CM, Kou Y, Duan Q, Wang Z, Meirelles GV, Clark NR, Ma'ayan A.
Enrichr: interactive and collaborative HTML5 gene list enrichment analysis tool. BMC Bioinformatics. 2013; 128(14).



