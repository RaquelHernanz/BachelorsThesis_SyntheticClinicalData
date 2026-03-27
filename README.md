# *BachelorsThesis_SyntheticClinicalData*

### `Title:` Generation and validation of synthetic data from clinical data in a hospital emergency department 
---
### `Author:` *Raquel Hernanz Hernández*
---
### `Degree:` Biomedical Engineering
---
### `Supervisors:` *José María Herrera* and *Guillermo José Ortega*
---
### `Entities:` Superior Polytechnic School, CEU San Pablo, Madrid; Biomedical Research Foundation of La Princesa University Hospital, Madrid.  
---
### `Brief description:` Bachelor Thesis repository based on the generation of synthetic clinical data from the Emergency Department at La Princesa University Hospital
---
### `Contents of the repository`
> #### - Dataset modifications.
> #### - Exploratory Data Analysis.
> #### - Unsupervised Machine Learning (Clustering).
> #### - Feature selection based on VIF and AIC on Logistic Regresion (LR).
> #### - Risk Score System.
> #### - Synthetic Data Generation based on two generator models: CTAB-GAN+ and ARF.
> #### - Evaluation of the Synthetic Data (fidelity, utility based on model performance, privacy and re-identification risk). 

### `Pipelines`
> #### - Preprocessing -- Notebooks 1, 2, 3, 4
> #### - Synthetic Data Generation Pipeline -- Notebooks 5, 6, 7
> #### - Evaluation of Synthetic Data -- Notebooks 8, 9, 10

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




