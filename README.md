# *BachelorsThesis_SyntheticClinicalData*

### `Title:` Generation and validation of synthetic data from clinical data in a hospital emergency department 
---
### `Author:` *Raquel Hernanz Hernández*
---
### `Degree:` Biomedical Engineering
---
### `Supervisors:` *José María Herrera* and *Guillermo José Ortega*
---
### `Entities:` Superior Polytechnic School, CEU San Pablo, Madrid; Health Research Institute (IIS-IP) at Hospital Universitario de La Princesa, Madrid.  
---
### `Brief description:` Bachelor Thesis repository based on the generation of synthetic clinical data from the Emergency Department at Hospital Universitario de La Princesa
---
### `Contents of the repository`
> #### - Dataset modifications.
> #### - Exploratory Data Analysis.
> #### - Unsupervised Machine Learning for Patient Profiling (Clustering).
> #### - Feature selection based on VIF and AIC on Logistic Regresion (LR).
> #### - Risk Score Systems.
> #### - Synthetic Data Generation based on two generator models: CTAB-GAN+ and ARF.
> #### - Evaluation of the Synthetic Data (fidelity, utility based on model performance, privacy and re-identification risk).

---

### `Workflow`
| Notebook | Title | Input | Output |
|----------|-------|-------|--------|
| **NB1** | Dataset Transformations prior to EDA | `raw_dataset.xlsx` | `dataset_FINAL.csv` |
| **NB2** | Exploratory Data Analysis and Unsupervised Patient Profiling | `dataset_FINAL.csv` | Descriptive statistics, clustering labels |
| **NB3** | Outlier Detection and Clinical Plausibility Audit | `dataset_FINAL.csv` | Outlier flags, audit report |
| **NB4** | VIF, AIC/BIC on Logistic Regression, and Risk Scoring System | `dataset_FINAL.csv` | Risk score, model coefficients, validation metrics |
| **NB5** | Pre-Generation Data Transformations | `dataset_FINAL.csv` | Stratified cohort files per mortality stratum |
| **NB6** | Synthetic Data Generation — CTAB-GAN+ | `dataset_PREGEN.csv` | Synthetic datasets × 10 replicas |
| **NB7** | Synthetic Data Generation — ARF/FORDE | `dataset_FINAL.csv` | Synthetic datasets × 10 replicas |
| **NB8** | Fidelity and Replicability Evaluation | Real + 10 synthetic datasets | Univariate/multivariate fidelity metrics, replicability report |
| **NB9** | Utility Evaluation — TSTR | Real + 10 synthetic datasets | Model performance comparison (AUC, calibration) |
| **NB10** | Privacy and Re-identification Risk | Real + 10 synthetic datasets | Distance-to-closest-record, membership inference metrics |

---
### `How to run the notebooks`

> **Step 1 — Mount Google Drive** (executed automatically by each notebook). Although it is not necesary for accesing the `/content` folder, it is essential for exporting tables and plots to Google Drive (`/content/drive/MyDrive/Colab Notebooks/TFG`). Should be noted the source and synthetic datasets are kept locally in the Data Analysis Unit computer and only uploaded temporary to the `/content` folder when executing the notebooks. 
 
> **Step 2 — Edit paths** in the `SHARED CONFIGURATION` cell of each notebook (Section 2). For example: 
RAW_DATA_PATH   = "/content/..."   # Path to raw Excel file (NB1 only)

> **Step 3 — Execute notebooks in order**: NB1 → NB2 / NB3 / NB4 (parallel) → NB5 → NB6 / NB7 (parallel) → NB8 / NB9 / NB10 (parallel). The notebook loads the output of its predecessor. Running them out of order will raise a `FileNotFoundError`.

---
### `Environment and dependencies`

> All notebooks run on **Google Colab** with Google Drive mounted at `/content/drive/`.
> No local installation is required beyond a standard Google account.
>
> Pre-installed in Colab (no action needed): `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`.
>
> **Non-standard dependency** — install once before running NB2:
> ```python
> !pip install prince>=0.13 -q   # Required for FAMD 
> ```
>
> **Generative models** — install before running NB6 and NB7 respectively:
> ```python
> !pip install ctabgan -q        # NB6 — CTAB-GAN+
> !pip install arfpy -q          # NB7 — ARF/FORDE
> ```

---
### `Data availability`

> The raw clinical dataset originates from the Health Research Institute (IIS-IP) at Hospital Universitario de La Princesa
> The raw dataset is **not included** in this repository due to patient privacy regulations (GDPR, Spanish Organic Law 3/2018). Access requests should be directed to the corresponding supervisor of the IIS-IP.
> The repository contains only notebook code. No patient data, identifiers, dataset replicates, or derived individual-level records are shared.


### `Abstract:`
> The use of real clinical data for research and educational purposes is constrained by legal and ethical restrictions related to patient privacy, particularly in sensitive environments such as hospital emergency departments. These limitations hinder the development and validation of data-driven predictive models.
The objective of this bachelor Thesis is to develop a synthetic data generator based on real clinical data from a hospital emergency department, aiming to preserve the relevant statistical characteristics of the original data while reducing the risk of patient reidentification.
The proposed methodology includes the selection and preprocessing of demographic, clinical, and care-related variables, followed by the generation of synthetic data using baseline statistical models and advanced generative models for tabular data. The evaluation strategy is based on statistical comparisons between real and synthetic datasets, utility analysis through training predictive models on synthetic data and testing them on real data, and privacy-oriented risk metrics.
This work aims to assess the feasibility of synthetic data as a safe alternative for clinical research and education, particularly in scenarios where access to real patient data is highly restricted.


### `Resumen:`
> El uso de datos clínicos reales en investigación y docencia está limitado por restricciones legales y éticas relacionadas con la privacidad del paciente, especialmente en entornos sensibles como los servicios de urgencias hospitalarias. Estas limitaciones dificultan el desarrollo y validación de modelos predictivos basados en datos reales.
El objetivo de este Trabajo Fin de Grado es desarrollar un generador de datos sintéticos a partir de datos clínicos reales procedentes de un servicio de urgencias hospitalarias, con el fin de preservar las características estadísticas relevantes de los datos originales y reducir el riesgo de reidentificación de los pacientes.
La metodología propuesta incluye la selección y el preprocesamiento de variables demográficas, clínicas y asistenciales, así como la generación de datos sintéticos mediante modelos estadísticos de referencia y modelos generativos avanzados para datos tabulares. La evaluación del conjunto sintético se plantea mediante comparaciones estadísticas entre datos reales y sintéticos, análisis de utilidad entrenando modelos predictivos en datos sintéticos y evaluándolos sobre datos reales, y métricas orientadas a la preservación de la privacidad.
Este trabajo pretende analizar la viabilidad del uso de datos sintéticos como una alternativa segura para la investigación y la docencia en el ámbito clínico, particularmente en contextos con fuertes restricciones de acceso a datos reales.




