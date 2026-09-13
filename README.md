# Supplementary Datasets for the Manuscript

## An Analytical Family of Correlation-Weighted Elastic-Net Estimators for the Conway–Maxwell–Poisson Regression Model

This repository contains the datasets used in the analyses reported in the associated manuscript:

> **An Analytical Family of Correlation-Weighted Elastic-Net Estimators for the Conway–Maxwell–Poisson Regression Model**

### Authors

**Ibrahim M. Taha<sup>a,b</sup>, Amany M. Mousa<sup>a</sup> and Mohamed R. Abonazel<sup>a</sup>**

<sup>a</sup> Department of Applied Statistics and Econometrics, Faculty of Graduate Studies for Statistical Research, Cairo University, Giza 12613, Egypt

<sup>b</sup> Department of Mathematics, Statistics and Insurance, Faculty of Management Sciences, Sadat Academy for Management Sciences, Corniche El-Nil, Maadi, Cairo 2222, Egypt

The datasets are provided to support transparency, reproducibility, and independent verification of the statistical analyses presented in the manuscript.

---

## Repository Contents

```text
.
├── README.md
├── CITATION.cff
└── data/
    ├── 11_Ant_abundance_Australia.xlsx
    ├── 16_Mollusk_communities.xlsx
    ├── docvisits.xlsx
    └── CrohnD.xlsx
```

## Datasets

### 1. Ant Abundance – Australia

**File:** `11_Ant_abundance_Australia.xlsx`

This dataset contains abundance data for an epigaeic ant species together with CLR-transformed abundances of co-occurring ant species and habitat variables.

- Observations: 30
- Predictors: 45
- Response: `Monomorium.leae`
- Source R package: `mvabund`
- R package version used in the prepared dataset: 4.2.8

The workbook contains documentation and variable-mapping information describing the variables and preprocessing.

Because CLR-transformed predictors are compositional, they are subject to the sum-to-zero constraint. This should be considered when interpreting the predictor structure.

**Primary source citation:**

Gibb, H., Stoklosa, J., Warton, D. I., Brown, A. M., Andrew, N. R. and Cunningham, S. A. (2015). Does morphology predict trophic position and habitat use of ant species and assemblages? *Oecologia*, 177, 519–531.

---

### 2. Mollusk Communities

**File:** `16_Mollusk_communities.xlsx`

This dataset contains mollusk abundance data together with CLR-transformed abundances of non-focal species and site, season, method, and duration covariates.

- Observations: 163
- Predictors: 30
- Source R package: `PLNmodels`
- Dataset: `mollusk`

The prepared dataset includes preprocessing and derived variables used for the statistical analysis. The workbook contains documentation and variable-mapping information.

Because CLR-transformed predictors are compositional, they satisfy a sum-to-zero constraint and may exhibit structural multicollinearity.

**Primary source citation:**

Richardot-Coulet, M., Chessel, D. and Bournaud, M. (1986). Typological value of the benthos of old beds of a large river. Methodological approach. *Archiv fur Hydrobiologie*, 107, 363–383.

---

### 3. Doctor Visits

**File:** `docvisits.xlsx`

This dataset contains the number of doctor visits during the previous three months together with demographic, socioeconomic, employment, insurance, and health-related covariates.

- Observations: 1,812
- Response: `docvisits`
- Source R package: `zic`

The dataset is based on data from the German Socioeconomic Panel and is documented in the `zic` R package.

**Primary source citation:**

Riphahn, R. T., Wambach, A. and Million, A. (2003). Incentive effects in the demand for health care: a bivariate panel count data estimation. *Journal of Applied Econometrics*, 18(4), 387–405.

---

### 4. Crohn's Disease Adverse Events

**File:** `CrohnD.xlsx`

This dataset contains adverse-event counts and patient-level covariates from a study involving patients with Crohn's disease.

- Observations: 117
- Variables: 9
- Response: `nrAdvE`

The dataset is documented in the `robustbase` R package.

**Primary source citation:**

Lo, S. N. and Ronchetti, E. (2006). Robust Second Order Accurate Inference for Generalized Linear Models. Technical report, University of Geneva, Switzerland.

---

## Data Preparation

The datasets are provided in Excel (`.xlsx`) format.

Some files contain transformed or derived variables prepared for the analyses in the associated manuscript. Therefore, these files should not necessarily be considered identical copies of the original datasets distributed through the corresponding R packages.

For the ant and mollusk datasets, the workbooks contain additional documentation sheets describing data sources, variable roles, and/or preprocessing.

The datasets are supplied specifically as supplementary research materials for the manuscript identified above.

## Reproducibility

The purpose of this repository is to make the data used in the manuscript available to researchers, reviewers, and readers for reproducibility and independent verification.

Researchers using these datasets should cite:

1. The associated manuscript; and
2. The primary source citation for each dataset listed above.

Where appropriate, users should also acknowledge the R package through which the dataset was obtained.

## Citation

Please cite the associated manuscript as follows:

> Taha, I. M., Mousa, A. M., & Abonazel, M. R. *An Analytical Family of Correlation-Weighted Elastic-Net Estimators for the Conway–Maxwell–Poisson Regression Model*.

**Publication details:** To be updated after acceptance/publication.

**DOI:** To be added when available.

## Data Provenance and Licensing

The datasets originate from previously published studies and/or publicly distributed R packages.

The primary source citations listed above were taken from the dataset citation/source documentation supplied with the prepared datasets.

Users should consult the original sources and applicable package/data licenses before redistributing or reusing third-party data.

The repository authors' documentation and other original materials are provided for research reproducibility. Any third-party dataset remains subject to the terms and attribution requirements of its original source.

No claim of ownership is made over third-party datasets.

## Contact

**Corresponding author:** Ibrahim M. Taha

**Email:** ibrahim.taha@sadatacademy.edu.eg; ibrahimaboalazm@gmail.com

**Affiliation:** Department of Applied Statistics and Econometrics, Faculty of Graduate Studies for Statistical Research, Cairo University, Giza 12613, Egypt

---

## Disclaimer

These datasets are provided for academic research and reproducibility purposes. Please refer to the associated manuscript and original data sources for the authoritative description of data collection, measurement, and study design.
