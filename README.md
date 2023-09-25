![Logo of the project](https://cienciadedatosysalud.org/wp-content/uploads/CONCEPT-h-color.png)

# CONCEPT-DIABETES 
CONCEPT-DIABETES is a project that focuses on assessing the effectiveness of a set of clinical practice actions and quality improvement strategies at different levels (patient-level, health-care provider level and health system level) on the management and health results of patients with type 2 diabetes (T2D) using Real World Data (RWD) routinely collected by five Spanish Regional Health Systems.

### CONCEPT Project Coordinator
**[Berta Ibáñez Beroiz PhD](https://orcid.org/0000-0002-7797-4845)**


## Analytical pipeline

## Outputs
Outputs structure and content is described below including the files and folders that are generated when creating a research project with the `cdmb` Python library. There are four main folders corresponding to:

- __docs/CDM/__
  - **cdmb_config.json**: Configuration file.
  - **cohort_definition_inclusion.csv**: csv file that defines the criteria (i.e., codes) for inclusion in a cohort.
  - **cohort_definition_exclusion.csv**: csv file that defines the criteria (i.e., codes) for exclusion in a cohort.
  - **common_datamodel.xlsx**: The definition of the common data model in Excel format.
  - **entities/**: Folder structure where, for each defined entity, the catalogs and the established validation rules are stored.
  - **ER.gv, ER.gv.png**: an Entity-Relationship Diagram of the entities included in the CDM.
  - **synthetic-data/**: Folder structure contaning an automatically generated set of 1000 synthetic records per entity included en the CDM.
  - **hashed_files_list.json**: List of the files generated or used after generating the project with their md5 hash. This file must be kept hidden 
and should be used to cross-check with the results obtained from the analysis from the original input files.
- __inputs/__
  - **data.duckdb**: Database that temporarily contains the data entered by the user (synthetic data by default)
- __outputs/__
  - (Default directory of all the outputs produced in the project execution)
- __src/__
  - __analysis-scripts/__
    - (directory where the analysis scripts developed by the user are stored)
    - **analytical_pipeline.qmd**: Quarto document containing the entire analytical pipeline (code, results and information on the analysis methodology followed).
    - **diabetes_drugs.csv**: Table with diabetes drugs' information.
    - **CIE9.csv**: Table with from CIE9 to CIAP2 translation information.
    - **CIE10.csv**: Table with from CIE10 to CIAP2 translation information.
    - **petri_net.pnml**: DM2 Treatment Algorithm's interpretation to patients with frailty in Petri net format.
    - **_quarto.yml**: File containing the Metadata to execute Quarto documents.
  - __check_load-scripts/__
    - **check_load.py**: Script in charge of the mapping between the files introduced by the user (./inputs) and map them to the defined entities (inputs/data.duckdb). 
    In the loading process, the following checks are performed: Name of the variables match; the format/type of the variables match those established in the configuration.
    - __inputs/__: Auxiliary folder for the script 'check_load.py'.
  - __dqa-scripts/__
    - **dqa.py**: Data Quality Assesment script by default.
  - **validation-scripts/**
    - **validator.py**: Script in charge of applying the validation rules to the data.
    - **valididator_report.qmd**: Quarto document that generates a report in html from the results obtained from 'validator.py'. 
    - **_quarto.yml**: File containing metadata to execute Quarto documents.
- **ro-crate-metadata.json**: Accessible and practical formal metadata description for use in a wider variety of situations, 
from an individual researcher working with a folder of data, to large data-intensive computational research environments. For more information, visit [RO-Crate](https://www.researchobject.org/ro-crate/).
- **man_container_deployment.md**: From Data Science for Health Services and Policy Research group we provide in the following
  GitHub repository, a solution, for the deployment of the generated project. This step is optional.
- **LICENSE.md**: Project license.


## R dependencies
Version of Rbase used: **4.2.3**

Version of [Quarto](https://quarto.org/) used: **1.3.361**

| library  |  version  | link |
|---|---|---|
| tidyverse  | 2.0.0	 | https://doi.org/10.21105/joss.01686  |
| lubridate  | 1.9.2	 | https://github.com/tidyverse/lubridate  |
| jsonlite  | 1.8.4	 | 	https://jeroen.r-universe.dev/jsonlite  |
| ggplot2  | 3.4.2	 | https://github.com/tidyverse/ggplot2  |
| bupaR  | 0.5.3	 | https://bupar.net/  |
| processmapR  | 0.5.3	 | https://github.com/bupaverse/processmapR  |
| dplyr  | 1.1.2	 | 	https://dplyr.tidyverse.org  |
| DiagrammeR  | 1.0.10	 | https://github.com/rich-iannone/DiagrammeR  |
| DiagrammeRsvg  | 0.1	 | 	https://github.com/rich-iannone/DiagrammeRsvg  |
| rsvg  | 2.4.0	 | 	https://docs.ropensci.org/rsvg/  |
| here  | 1.0.1	 | https://here.r-lib.org/  |
| reticulate  | 1.32.0	 | https://github.com/rstudio/reticulate  |


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
| dateutil  | 2.8.2  | [https://www.scikit-yb.org/en/latest/](https://pypi.org/project/python-dateutil/)  |

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
