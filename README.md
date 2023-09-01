![Logo of the project](https://cienciadedatosysalud.org/wp-content/uploads/CONCEPT-h-color.png)

# CONCEPT-DIABETES 
CONCEPT-DIABETES is a project that focuses on assessing the effectiveness of a set of clinical practice actions and quality improvement strategies at different levels (patient-level, health-care provider level and health system level) on the management and health results of patients with type 2 diabetes (T2D) using Real World Data (RWD) routinely collected by five Spanish Regional Health Systems.

### CONCEPT Project Coordinator
**[Berta Ibáñez Beroiz PhD](https://orcid.org/0000-0002-7797-4845)**


## Analytical pipeline

### Project structure
```shell
.
├── Algoritmo_DM2_ENG_2023.pdf
├── analytical_pipeline.qmd
├── analytical_pipeline.html
├── inputs
│   ├── CIE9.csv
│   ├── CIE10.csv
│   ├── diabetes_drugs.csv
│   ├── dm_cmbd_df.csv
│   ├── dm_comorb.csv
│   ├── dm_param_df.csv
│   ├── dm_patients_df.csv
│   ├── dm_treat_df.csv
│   └── FRAG_HBA.pnml
├── LICENSE
├── outputs
│   ├── activity_presence.png
│   ├── barplot_features_importance.png
│   ├── decision_tree.png
│   ├── dendogram.png
│   ├── dm_cmbd_df.csv
│   ├── dm_comorb.csv
│   ├── dm_param_df.csv
│   ├── dm_patients_df.csv
│   ├── dm_treat_df.csv
│   ├── eventlog.csv
│   ├── eventlog.xes
│   ├── eventlog_filtered.csv
│   ├── eventlog_filtered.xes
│   ├── eventlog_raw.csv
│   ├── evlog_pm_02.png
│   ├── evlog_pm_1.png
│   ├── evlog_pm_cluster_0.png
│   ├── evlog_pm_cluster_1.png
│   ├── evlog_pm_cluster_2.png
│   ├── evlog_pm_cluster_5.png
│   ├── evlog_pm_cluster_3.png
│   ├── evlog_pm_cluster_7.png
│   ├── evlog_pm_cluster_8.png
│   ├── evlog_pm_cluster_9.png
│   ├── evlog_pm_cluster_11.png
│   ├── fitness_by_cluster.csv
│   ├── fitness_by_cluster.png
│   ├── trace_0.png
│   ├── trace_1.png
│   ├── trace_2.png
│   ├── trace_5.png
│   ├── trace_7.png
│   ├── trace_8.png
│   ├── trace_6.png
│   └── trace_9.png
│   └── trace_11.png
├── petri_net.png
└── README.md


```
#### Main files

- **analytical_pipeline.qmd**: Quarto document containing the entire analytical pipeline (code, results and information on the analysis methodology followed).
- **analytical_pipeline.html**: Output self-contained HTML file containing the analysis results and additional project information.
- **diabetes_drugs.csv**: Table with diabetes drugs' information.
- **CIE9.csv**: Table with from CIE9 to CIAP2 translation information.
- **CIE10.csv**: Table with from CIE10 to CIAP2 translation information.
- **dm_cmbd_df.csv**: Synthetic data of hospitalizations table compliant with the Common Data Model.
- **dm_comorb_df.csv**: Synthetic data of comorbidities table compliant with the Common Data Model.
- **dm_param_df.csv**: Synthetic data of parameters table compliant with the Common Data Model.
- **dm_patients_df.csv**: Synthetic data of patients compliant with the Common Data Model.
- **dm_treat_df.csv**: Synthetic data of treatments compliant with the Common Data Model.
- **FRAG_HBA.pnml**: DM2 Treatment Algorithm's interpretation to patients with frailty in Petri net format.

## R dependencies
Version of Rbase used: **4.2.3**

Version of [Quarto](https://quarto.org/) used: **1.3.361**

| library  |  version  | link |
|---|---|---|
| tidyverse  | 2.0.0	 | https://doi.org/10.21105/joss.01686  |
| lubridate  | 1.9.2	 | https://github.com/tidyverse/lubridate  |
| mongolite  | 2.7.2	 | 	https://github.com/jeroen/mongolite  |
| jsonlite  | 1.8.4	 | 	https://jeroen.r-universe.dev/jsonlite  |
| ggplot2  | 3.4.2	 | https://github.com/tidyverse/ggplot2  |
| bupaR  | 0.5.3	 | https://bupar.net/  |
| processmapR  | 0.5.3	 | https://github.com/bupaverse/processmapR  |
| dplyr  | 1.1.2	 | 	https://dplyr.tidyverse.org  |
| DiagrammeR  | 1.0.10	 | https://github.com/rich-iannone/DiagrammeR  |
| DiagrammeRsvg  | 0.1	 | 	https://github.com/rich-iannone/DiagrammeRsvg  |
| rsvg  | 2.4.0	 | 	https://docs.ropensci.org/rsvg/  |
| here  | 1.0.1	 | https://here.r-lib.org/  |


## Python dependencies
Version of Python used: **3.9**
| library  |  version  | link |
|---|---|---|
| pm4py  | 2.7.4  | https://pm4py.fit.fraunhofer.de/  |
| datetime  | 5.1  |https://docs.python.org/3/library/datetime.html   |
| pandas  | 1.4.4  | https://pandas.pydata.org/  |
| numpy  | 1.23.5  | https://numpy.org/  |
| itertools  |  8.12.0  | https://docs.python.org/3/library/itertools.html  |
| matplotlib  |  3.7.1  | https://matplotlib.org/  |
| texdistance  | 4.2.1  | https://github.com/life4/textdistance  |
| gensim  | 4.3.1  | https://github.com/RaRe-Technologies/gensim  |
| scipy  | 1.10.1  | https://scipy.org/  |
| scikit-learn  | 1.2.2  | https://scikit-learn.org/stable/  |
| yellowbrick  | 1.5  | https://www.scikit-yb.org/en/latest/  |


## Usage

Run it with your favorite IDE, for example Rstudio.

Follow the steps below to render once the analysis_concept.qmd file is opened in Rstudio:

https://quarto.org/docs/get-started/hello/rstudio.html

Or, once the dependencies have been correctly installed, run in terminal: 

```shell
quarto analytical_pipeline.qmd
```

## Links

- Common Data Model: https://zenodo.org/record/8093865

## How to contribute

- Issue tracker: https://github.com/metodologianavarrabiomed/CONCEPT-DIABETES/issues
- Repository: https://github.com/metodologianavarrabiomed/CONCEPT-DIABETES

 
<a href="https://creativecommons.org/licenses/by/4.0/" target="_blank" ><img src="https://img.shields.io/badge/license-CC--BY%204.0-lightgrey" alt="License: CC-BY 4.0"></a>
