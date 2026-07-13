# Human therapy-induced senescence — single-cell & bulk RNA-seq

Single-cell (10x Chromium) and bulk RNA-seq analysis of **therapy-induced senescence in human
cells**, comparing **vehicle (control)** vs **docetaxel (Doce)** treatment.

## Analysis
- `scripts/scRNAseq/01_..preprocessing.Rmd` — QC, normalisation, clustering, annotation
- `scripts/scRNAseq/02_..overview.Rmd` — dataset overview and senescence-programme visualisation

## Data
CellRanger output and processed objects are kept outside version control (available on request /
archived externally).

---
Analysis by **Dillon Corvino** · [GitHub](https://github.com/Eomesodermin) · [dilloncorvino.com](https://dilloncorvino.com)

## Environment

Built in **R** with a Seurat-based single-cell stack — key packages: `Seurat`, `SeuratDisk`, `scCustomize`, `dplyr`, `ggplot2`, `Azimuth`, `SeuratData`, `SeuratWrappers`, `gplots`, plus my helper package [`r-utility-functions`](https://github.com/Eomesodermin/r-utility-functions).

A pinned `renv.lock` is **not** committed for this repository. To capture an exact, reproducible
environment, run in the project root:

```r
install.packages("renv")
renv::init()        # discovers dependencies from the scripts
renv::snapshot()    # writes renv.lock pinning every package version
```
