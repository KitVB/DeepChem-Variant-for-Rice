# Rice Drought-Response Gene Variant Effect Prediction Pipeline

## Overview

This repository contains a complete computational pipeline for predicting the functional impact of genetic variants in rice (*Oryza sativa*) genes using DeepChem-variant

## Repository Contents

### Files Included

1. **`deepvariant_case_study_rice_osdreb2a.ipynb`**
   - Complete Jupyter notebook with full pipeline implementation
   - Runnable in Google Colab (GPU recommended)

2. **`best_model (1).pth`** 
   - Pre-trained DeepChem-Variant model weights
   - Trained on indica rice subspecies variants
   - 95.3% accuracy on validation set
   - Can be used for transfer learning to other rice varieties


## Required Data Files

Download the following files from **RAP-DB** (Rice Annotation Project Database):

**Download URL**: https://rapdb.dna.affrc.go.jp/download/irgsp1.html

Required files:
1. **Reference Genome** (FASTA format)
   - File: `IRGSP-1.0_genome.fasta.gz`
   - Description: Complete rice reference genome sequence

2. **Gene Annotations** (GTF/GFF format)
   - File: `IRGSP-1.0_representative_annotation_*.gtf.gz`
   - Description: Gene structure and coding sequence annotations

3. **CDS Sequences** (FASTA format)
   - File: `IRGSP-1.0_cds_*.fasta.gz`
   - Description: Coding sequences for all annotated genes

4. **Protein Sequences** (FASTA format)
   - File: `IRGSP-1.0_protein_*.fasta.gz`
   - Description: Translated protein sequences


## Model Performance

| Dataset | Accuracy | Precision | Recall | F1-Score |
|---------|----------|-----------|--------|----------|
| Training/Validation (indica) | 95.37% | 95.29% | 95.37% | 95.32% |
| Test Set (same subspecies) | 95.30% | 95.39% | 95.30% | 95.32% |
| Test Set (different subspecies) | 95.94% | 96.06% | 95.94% | 95.98% |