# 1. In Vitro CRISPR Screen Analysis for Identifying Synthetic Lethal Targets to MYC inhibitors
This repository contains the computational pipeline for analyzing genome-wide CRISPR screening data to identify synthetic lethal interactions with MYC inhibition. 
The pipeline combines MAGeCK and DrugZ analyses for robust hit identification.

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

## Introduction / Overview

This pipeline was developed to pinpoint genes whose loss enhances or diminishes sensitivity to the small-molecule MYC inhibitor **MYCi975**. We used an unbiased, genome-wide CRISPR screening approach and validated hits using multiple downstream analyses.  
Key features of this workflow include:

- **High-throughput data processing** of FASTQ reads  
- **Guide quantification** and **normalization** using MAGeCK  
- **Hit-calling** and **synergy detection** with DrugZ  
- **Functional interpretation** via custom R scripts for plotting and **pathway enrichment**  

Follow the steps below to reproduce the key analyses or adapt them to your CRISPR screen data.

---

