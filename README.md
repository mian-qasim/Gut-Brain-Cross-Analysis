# Predicting Spaceflight-Induced Neuroinflammation via Computational Metabolite Inference

Cross-analysis of publicly available mouse spaceflight multi-omics data from the gut and brain, identifying reproducible relationships between gut microbiome alterations and brain neuroinflammatory signatures. A literature-informed inferred serum layer will be constructed to investigate whether circulating molecular changes can serve as an intermediary between the gut and brain. relationships will then be used to develop a predictive model assessing whether gut microbiome changes can predict downstream serum and brain responses.

## 🎯 Research Question
*“Can spaceflight-induced gut microbiome alterations be used to predict brain neuroinflammatory signatures through a literature-informed inferred serum intermediary using integrated multi-omics analysis?”*

## 📊 Audited Sample Matrix Framework
This pipeline cleans and integrates **70 highly curated, untreated Wild Type samples** across 6 distinct NASA flight payloads:

### 🦠 Gut Axis (Fecal Metagenomics)
- **OSD-466 (RR-10):** Stool Matrix | Whole-Genome Shotgun Sequencing | Filter: Wild Type Only (Drop p21-null)
- **OSD-249 (RR-6):** Stool Matrix | Whole-Genome Shotgun Sequencing | Filter: Sham Controls Only (Drop treated)
- **Total Gut Cohort:** 40 samples (19 Spaceflight vs. 21 Ground Controls)

### 🧠 Brain Axis (Neuro-Transcriptomics)
- **OSD-612 (RR-10):** Left Hemisphere | Bulk RNA Sequencing | Filter: Wild Type Only (Drop p21-null)
- **OSD-613 (RRRM-2):** Left Hemisphere | Bulk RNA Sequencing | Filter: Baseline Terminal Only (Drop recovery LAR)
- **OSD-352 (RR-3):** Brain Hippocampus | Bulk RNA Sequencing | Filter: Sham Controls Only (Drop treated)
- **OSD-682 (RR-18):** Brain Hippocampus | Spatial Transcriptomics | Filter: Vehicle Controls Only (Drop BuOE treated)
- **Total Brain Cohort:** 39 samples (19 Spaceflight vs. 20 Ground Controls)

## 🛠️ Methodological Stack
- **Data Integration:** Pandas metadata filtering, string-matching cohort alignment, group-averaging meta-analysis.
- **Serum Layer:** Computational Metabolite Inference loop converting Metagenomic inputs into an Inferred Blood Metabolite Matrix.
- **Machine Learning:** `scikit-learn` Principal Component Analysis (PCA) for global dimensionality reduction and `RandomForestRegressor` for unbiased multi-system feature importance ranking.
- **Visualization:** Interactive Plotly graphics hosted via a web-deployed Streamlit application.

## 📜 License
This project is licensed under the permissive open-source **MIT License**—see the `LICENSE` file for details.
