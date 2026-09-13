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

Every workbook contains a `Data` sheet holding the analysis matrix, with the response in the first column, named `y`, and one column per predictor. The two ecological workbooks also contain a `README` sheet recording the source, the preprocessing, and the response summaries, and a `VarMap` sheet giving the role of every column.

## Datasets

| File | n | p | Response | Source package |
| --- | ---: | ---: | --- | --- |
| `11_Ant_abundance_Australia.xlsx` | 30 | 45 | `Monomorium.leae` | `mvabund` |
| `16_Mollusk_communities.xlsx` | 163 | 29 | `Bit` | `PLNmodels` |
| `docvisits.xlsx` | 1,812 | 22 | `docvisits` | `zic` |
| `CrohnD.xlsx` | 117 | 8 | `nrAdvE` | `robustbase` |

Here `p` counts predictor columns, excluding the response.

---

### 1. Ant Abundance – Australia

**File:** `11_Ant_abundance_Australia.xlsx`

Abundance of one epigaeic ant species across 30 sites in south-eastern Australia, together with centred log-ratio (CLR) abundances of the 40 co-occurring species and 5 measured habitat variables.

- Observations: 30
- Predictors: 45 (40 CLR co-abundances, 5 habitat variables)
- Response: `Monomorium.leae`
- Source: `mvabund::antTraits`, package version 4.2.8

The response species is excluded from the CLR closure, so no predictor is an algebraic function of the response. Because the CLR predictors are compositional, they satisfy a sum-to-zero constraint by construction; together with p > n this makes the cross-product matrix exactly singular, and it is the source of the multicollinearity reported in the manuscript. No log total count is exported.

The response was fixed a priori. The most abundant species detected in at least 30 percent of sites, `Iridomyrmex.rufoniger`, is right-censored at 20 with 9 of the 30 sites at the cap, which makes it unsuitable for an unbounded count model.

**Primary source citation:**

Gibb, H., Stoklosa, J., Warton, D. I., Brown, A. M., Andrew, N. R. and Cunningham, S. A. (2015). Does morphology predict trophic position and habitat use of ant species and assemblages? *Oecologia*, 177, 519–531.

---

### 2. Mollusk Communities

**File:** `16_Mollusk_communities.xlsx`

Abundance of one mollusk species across 163 samples, together with CLR abundances of the non-focal species and dummy-coded site, season and method covariates plus a numeric exposure duration.

- Observations: 163
- Predictors: 29 (17 CLR co-abundances, 11 covariate dummies, 1 numeric duration)
- Response: `Bit`
- Source: `PLNmodels::mollusk`

The response species is excluded from the CLR closure. Site, season and method are dummy-coded against an explicit baseline: `GGravier1`, `automn` and `string` respectively. As with the ant data, the CLR predictors satisfy a sum-to-zero constraint and are the source of the structural multicollinearity. No log total count is exported.

**Primary source citation:**

Richardot-Coulet, M., Chessel, D. and Bournaud, M. (1986). Typological value of the benthos of old beds of a large river. Methodological approach. *Archiv für Hydrobiologie*, 107, 363–383.

---

### 3. Doctor Visits

**File:** `docvisits.xlsx`

Number of doctor visits during the previous three months, together with demographic, socioeconomic, employment, insurance and health-related covariates.

- Observations: 1,812
- Predictors: 22
- Response: `docvisits`
- Source: `zic::docvisits`

The data are drawn from the German Socioeconomic Panel. Nine of the twenty-two predictors are functions of age, which is part of the published specification and the source of the collinearity in this application.

**Primary source citation:**

Riphahn, R. T., Wambach, A. and Million, A. (2003). Incentive effects in the demand for health care: a bivariate panel count data estimation. *Journal of Applied Econometrics*, 18(4), 387–405.

---

### 4. Crohn's Disease Adverse Events

**File:** `CrohnD.xlsx`

Adverse-event counts and patient-level covariates from a study of patients with Crohn's disease.

- Observations: 117
- Predictors: 8
- Response: `nrAdvE`
- Source: `robustbase::CrohnD`

**Primary source citation:**

Lo, S. N. and Ronchetti, E. (2006). Robust Second Order Accurate Inference for Generalized Linear Models. Technical report, University of Geneva, Switzerland.

---

## Data Preparation

The datasets are supplied in Excel (`.xlsx`) format and are derived from the packaged data rather than being verbatim copies of it. The `docvisits` and `CrohnD` workbooks reproduce the packaged variables directly. In the ant and mollusk workbooks the response is one species column taken from the packaged abundance matrix, and the predictors are the CLR transform of the remaining species columns, computed with a pseudocount of 0.5 after removing species present in fewer than 5 percent of rows, together with the packaged environmental or design variables. The prevalence filter is applied to the predictor block only and never consults the response.

Every value in each workbook was checked element-wise against the corresponding packaged dataset. The `README` and `VarMap` sheets in the two ecological workbooks document the source, the transformation, and the role of every exported column.

## Reproducibility

The purpose of this repository is to make the data used in the manuscript available to researchers, reviewers and readers for reproducibility and independent verification.

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

The datasets originate from previously published studies distributed through publicly available R packages.

Users should consult the original sources and applicable package and data licences before redistributing or reusing third-party data.

The repository authors' documentation and other original materials are provided for research reproducibility. Any third-party dataset remains subject to the terms and attribution requirements of its original source.

No claim of ownership is made over third-party datasets.

## Contact

**Corresponding author:** Ibrahim M. Taha

**Email:** ibrahim.taha@sadatacademy.edu.eg; ibrahimaboalazm@gmail.com

**Affiliation:** Department of Applied Statistics and Econometrics, Faculty of Graduate Studies for Statistical Research, Cairo University, Giza 12613, Egypt

---

## Disclaimer

These datasets are provided for academic research and reproducibility purposes. Please refer to the associated manuscript and the original data sources for the authoritative description of data collection, measurement and study design.
