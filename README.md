# Overview

This project integrates metabolomics and transcriptomics data to characterize molecular changes during the interactions of four Streptomyces strains grown on interaction plates. The goal was to identify candidate genes, metabolites, and biological pathways potentially underlying antibacterial activity observed during co-cultivation.

A combination of high-throughput untargeted metabolomics (LC-MS/MS) and RNA-seq was employed. The project involves pre-processing, annotation, and integrative analysis, using both R and Python workflows.

Experimental Design
Organisms: Four distinct Streptomyces strains.

Setup: Interaction plates where strains were cultured in proximity to induce molecular responses.
![image](https://github.com/user-attachments/assets/9e8d564f-b78f-440d-a13d-f4d3581d9fa2)


## Data Types:

Metabolomics: Positive and negative mode LC-MS/MS datasets.

Transcriptomics: RNA-Seq datasets, one per strain.

Aim: Identify differential features and pathways linked to antibacterial activity by combining omics layers.

The experimental metadata, feature information, and sample descriptions are fully incorporated into the analysis pipelines.

## Data Description

### Metabolomics Data
#### Two datasets:

metabolomics_pos.RData (positive mode)

metabolomics_neg.RData (negative mode)

#### Contents:

data_pos / data_neg: Mass spectrometry feature matrices (features × samples).

features_info: Feature metadata (m/z values, retention times).

samples_info: Sample metadata (strain identity, batch, day).

### Transcriptomics Data
#### Four datasets:

transcriptomics_strainA.RData, transcriptomics_strainB.RData, transcriptomics_strainC.RData, transcriptomics_strainD.RData

#### Contents:

counts: Raw gene count matrices (genes × samples).

genes_info: Gene metadata (locus tags, gene products).

samples_info: Sample metadata (strain, replicate, timepoint).

### Repository Structure
Metabolomics_positive_pipeline.qmd: Preprocessing and quality control pipeline for positive-mode metabolomics data.

Metabolomics_negative_pipeline.qmd: Preprocessing and quality control pipeline for negative-mode metabolomics data.

Annotations_metabolomics.qmd: Metabolite annotation and integration of feature information post-processing.

transcriptomics_strain_A_pipeline.qmd: Preprocessing and quality control pipeline for strain A transcriptomics data.

PathIntegrate_Analysis.ipynb: Multi-omics data integration analysis using PathIntegrate, including pathway enrichment and molecular candidate identification.

ipaPy2_annotation code.ipynb: Code for running pathway analysis and annotation using the ipaPy2 Python package.

### Tools and Dependencies
##### R (≥ 4.2.0)
tidyverse

limma

edgeR

pheatmap

ComplexHeatmap

MetaboAnalystR

##### Python (≥ 3.9)
pandas

numpy

scipy

pathintegrate

ipapy2

### How to Use
Preprocess the metabolomics and transcriptomics datasets (.qmd files).

Perform feature annotation (Annotations_metabolomics.qmd).

Conduct pathway-based integration analysis (PathIntegrate_Analysis.ipynb).

Annotate pathway results using ipaPy2_annotation code.ipynb.

Each notebook is modular and can be executed independently following the order above.

### Key Outcomes
Identification of differential metabolites and genes between interacting strains.

Multi-omics integration to prioritize biological pathways linked to antibacterial effects.

Establishment of a reproducible workflow for future multi-omics integration studies.

### Acknowledgements
This work was conducted as part of the MSc Bioinformatics research project at [Your University Name].
Supervised by Dr. Francesco Del Carratore.
