# 1. In Vitro CRISPR Screen Computational Pipeline for Identifying Synthetic Lethal Targets to MYC inhibitors (or any other inhibitors)
This repository provides a **step-by-step computational workflow** for analyzing **whole-genome CRISPR screening data**, from raw sequencing files to hit identification and pathway analysis.  
While this guide uses a **MYC inhibitor study** as an example, the methods described here are broadly applicable to **any CRISPR screen** investigating synthetic lethality, biomarker identification and combination drug strategies.  
This pipeline leverages **MAGeCK** and **DrugZ**, two widely used tools for CRISPR screen analysis, and provides detailed instructions for setup, execution, and interpretation of results.  

---

## Table of Contents
1. [Introduction / Overview](#introduction--overview)
2. [Merging FASTQs](#2-merging-fastqs)
3. [Quality Control](#3-quality-control)
4. [MAGeCK Setup](#4-mageck-setup)
5. [MAGeCK Count](#5-mageck-count)
6. [MAGeCK MLE](#6-mageck-mle)
7. [DrugZ Analysis](#7-drugz-analysis)
8. [Visualization](#8-visualization)
9. [Pathway Analysis](#9-pathway-analysis)

---

## Introduction / Overview / Experimental Design

This pipeline was developed to pinpoint genes whose loss enhances or diminishes sensitivity to the small-molecule MYC inhibitor **MYCi975**. We used an unbiased, genome-wide CRISPR screening approach and validated hits using multiple downstream analyses.  
Chemo-genomic screens are useful to identify combination strategies and biomarkers for clinical trials 

The screen involves the following key conditions:  

- **T0 (Baseline)** – Initial cell population before treatment  
- **T12 DMSO (Control)** – Cells treated with DMSO (vehicle) for 12 days  
- **T12 MYC Inhibitor (Treated)** – Cells treated with MYCi975 for 12 days  

By comparing guide RNA (gRNA) enrichment or depletion between these conditions, we can **identify genes that influence MYC inhibitor sensitivity**.  

Key features of this workflow include:

- **Pre-processing FASTQ files** (merging lanes, quality control)  
- **Guide quantification and normalization** (using MAGeCK)  
- **Hit identification** (MAGeCK MLE and DrugZ)  
- **Functional analysis and pathway enrichment** (Using R)

Follow the steps below to reproduce the key analyses or adapt them to your CRISPR screen data.

---

