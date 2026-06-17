# Systems-level phenomic and metabolomic profiling for New Approach Methodology-based hepatotoxicity assessment in fish

This repository contains the processed data tables and analysis scripts supporting the manuscript on integrated phenomic and metabolomic profiling of perfluorooctane sulfonic acid (PFOS), benzo[a]pyrene (BaP), bisphenol A (BPA), and their binary and ternary mixtures in two fish liver cell models: RTL-W1 and ZFL.

The study was designed as a mechanistic profiling and method-development framework for integrating Cell Painting phenomics with metabolomics/lipidomics in support of New Approach Methodologies (NAMs).
The exposure concentrations were selected to generate interpretable, non- or minimally cytotoxic perturbation profiles and should not be interpreted as environmentally realistic exposure levels or as a direct environmental risk assessment.

---

## Repository contents

The repository includes processed quantitative data tables for Cell Painting and LC-HRMS-based metabolomics/lipidomics, together with analysis scripts used for statistical analysis, visualization, and data integration.

### Cell Painting data

Two Cell Painting files are provided, one for each cell line:

| File | Description |
|---|---|
| `RTL_fish_cells_2025_Randomized_treatment_level_per_plate.xlsx` | Plate-level Cell Painting feature table for RTL-W1 cells |
| `ZFL_New_Fish_cells_2025_Randomized_treatment_level_per_plate.xlsx` | Plate-level Cell Painting feature table for ZFL cells |

These files contain plate-level aggregated morphological features extracted from Cell Painting assays. Features are organized according to CellProfiler-style feature names and include measurements associated with the main Cell Painting channels/compartments:

- DNA/nuclei
- RNA/nucleoli
- Endoplasmic reticulum (ER)
- Actin cytoskeleton/Golgi apparatus/plasma membrane (AGP)
- Mitochondria (Mito)

The values represent processed Cell Painting feature values used for downstream statistical analysis and visualization. Feature values were normalized against the corresponding DMSO control as described in the manuscript Methods section.

### Metabolomics and lipidomics data

Three LC-HRMS-derived data tables are provided:

| File | Description |
|---|---|
| `B014_JZ_CELLS_PFASBA_neg-FINAL (6).xlsx` | Semi-polar metabolite features measured in the cellular fraction |
| `B014_JZ_SUP_PFASBA_neg-FINAL (6).xlsx` | Semi-polar metabolite features measured in the supernatant fraction |
| `B014_JZ_CELL_LIP_pos-FINAL (3).xlsx` | Lipid features measured in the cellular fraction |

These files contain processed intensity matrices used for statistical analysis, pathway enrichment analysis, and integration with Cell Painting data. The files include identified compounds where available and non-annotated features represented by m/z-retention time pairs.

---

## Experimental overview

Two fish liver-derived cell lines were used:

- **RTL-W1**: rainbow trout liver cell line
- **ZFL**: zebrafish liver cell line

Cells were exposed to PFOS, BaP, BPA, and selected binary and ternary mixtures. DMSO-treated samples served as solvent controls. Cell viability was assessed before downstream profiling to select non- or minimally cytotoxic exposure concentrations. Cell Painting and metabolomics/lipidomics analyses were then performed to characterize compound- and mixture-associated phenotypic and metabolic responses.

---

## Data structure

Exact column names may differ slightly between files, but the data tables generally include the following information.

### Cell Painting files

Feature names follow CellProfiler-style naming conventions and encode the object, measurement type, and measured compartment/channel where applicable.

### Metabolomics/lipidomics files

Intensity columns contain normalized metabolite or lipid feature abundances used for downstream statistical analysis.

---

## Analysis workflow

The main analyses performed in the manuscript include:

1. **Cell viability assessment**  
   Selection of non- or minimally cytotoxic concentrations suitable for Cell Painting and metabolomics/lipidomics profiling.

2. **Cell Painting feature analysis**  
   Normalization against DMSO controls, feature-level statistical testing, dimensionality reduction, and visualization of phenotypic fingerprints.

3. **Metabolomics and lipidomics analysis**  
   Processing of semi-polar metabolite and lipid intensity matrices, statistical testing, and pathway enrichment analysis.

4. **Pathway enrichment analysis**  
   Pathway enrichment analysis was performed using the “MS Peaks to Pathways” module in MetaboAnalyst 6.0. Input data included identified compounds and non-annotated m/z-retention time features, together with statistical information such as p-values and fold-change-derived scores.

5. **Phenomics–metabolomics integration**  
   Cell Painting and metabolomics/lipidomics data were integrated to identify metabolite–phenotype associations and pathway-linked subcellular phenotypes.

---

---

## Raw data availability

The repository contains processed quantitative feature tables and intensity matrices used for analysis. Original raw microscopy image files from Cell Painting and raw LC-HRMS instrument files are not hosted directly in this repository due to file-size constraints.

Raw Cell Painting images and raw LC-HRMS files are available from the corresponding author upon reasonable request.

---

## Reproducibility notes

- Cell Painting data are provided as plate-level feature tables rather than raw single-cell image files.
- Metabolomics/lipidomics data are provided as processed intensity matrices after blank removal and quality-control assessment.
- Feature values and metabolite/lipid intensities should be interpreted according to the normalization procedures described in the manuscript Methods section.

---

## Citation

If you use this dataset or code, please cite the associated manuscript:

> [Insert manuscript citation here once available]

---

## Contact

For questions regarding the dataset, analysis scripts, raw Cell Painting images, or raw LC-HRMS files, please contact:

Jonas Zetzsche
Örebro University
jonas.zetzsche@oru.se

---

## License

Please specify the intended license for this repository. Recommended options include:

- MIT License for analysis code
- CC BY 4.0 for processed data tables

If no license is provided, reuse rights may be restricted by default.
