# Miriam Senescence — Human Dataset

## Project Summary

Analysis of human senescence data using single-cell and bulk RNA sequencing.
Experimental conditions: **Vehicle** (control) vs **Doce** (Docetaxel treatment).

## Dataset Info

| Dataset | Type | Conditions | Notes |
|---------|------|------------|-------|
| scRNAseq | 10x Chromium | Vehicle, Doce | CellRanger output |
| bulkRNAseq | — | — | TBD |

## File Structure

```
.
├── data/
│   ├── scRNAseq/
│   │   ├── Vehicle/          # CellRanger output — Vehicle condition
│   │   │   ├── raw_feature_bc_matrix/
│   │   │   ├── filtered_feature_bc_matrix/
│   │   │   └── analysis/     # CellRanger clustering/PCA/UMAP/tSNE
│   │   └── Doce/             # CellRanger output — Docetaxel condition
│   │       ├── raw_feature_bc_matrix/
│   │       ├── filtered_feature_bc_matrix/
│   │       └── analysis/
│   └── bulkRNAseq/           # Bulk RNAseq data (TBD)
│
├── scripts/
│   ├── scRNAseq/
│   │   ├── 01_Miriam_Human_dataset_preprocessing.Rmd   # QC, normalisation, integration
│   │   └── 02_Miriam_Human_dataset_overview.Rmd        # Visualisation, DEG, cell cycle
│   ├── bulkRNAseq/           # Bulk RNAseq analysis scripts (TBD)
│   ├── variables/
│   │   ├── Colour_scheme_variable.R
│   │   └── Gene_list_human.xlsx
│   ├── Load_Packages.R       # Shared package loading
│   └── Setup.R               # Shared environment setup
│
├── results/                  # Analysis outputs (gitignored; regenerated from scripts)
├── saves/                    # Seurat objects and intermediate saves (gitignored)
└── figures/                  # Reference figures
```

> **Note:** `results/` and `saves/` are gitignored. Large data files are tracked via Git LFS.
> Seurat objects and CellRanger output will be uploaded to Zenodo.

## Data Availability

- Raw data: GEO (link TBD)
- CellRanger output: Zenodo (link TBD)
- Seurat objects: Zenodo (link TBD)

## Author

- [Dillon Corvino](https://github.com/Eomesodermin)
