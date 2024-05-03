![Logo of the project](https://cienciadedatosysalud.org/wp-content/uploads/CONCEPT-h-color.png)

<small><i>This project follows the structure built using the [Common Data Model Builder](https://github.com/cienciadedatosysalud/cdmb), a tool that allows you to create common data models to facilitate interoperability and reproducibility of the analyses.</i></small>


# CONCEPT-DIABETES 
CONCEPT-DIABETES is a project that focuses on assessing the effectiveness of a set of clinical practice actions and quality improvement strategies at different levels (patient-level, health-care provider level and health system level) on the management and health results of patients with type 2 diabetes (T2D) using Real World Data (RWD) routinely collected by five Spanish Regional Health Systems.

## CONCEPT Project Coordinator
**[Berta Ibáñez Beroiz PhD](https://orcid.org/0000-0002-7797-4845)**

## Cohort definition:

The cohort is defined as patients with type 2 diabetes.

### Inclusion criteria: 

Patients that, at 2017-01-01 or during the follow-up from 2017-01-01 to 2022-12-31, had active health card (active TIA - tarjeta sanitaria activa) and one of the inclusion codes given in the ‘inclusion code list (’T90’ if CIAP-2, ‘250’ if ‘CIE-9CM’ or ‘E11’ if CIE-10-ES).

### Exclusion criteria: 

Patients that had none of the exclusion codes given in the exclusion codes list (‘T89’ if CIAP-2, ‘250.01’ if CIE-9CM, ‘250.03’ if CIE-9CM, ‘250.11’ if CIE-9CM, ‘250.13’ if CIE-9CM, ‘250.21’ if CIE-9CM, ‘250.23’ if CIE-9CM, ‘250.31’ if CIE-9CM, ‘250.33’ if CIE-9CM, ‘250.41’ if CIE-9CM, ‘250.43’ if CIE-9CM, ‘250.51’ if CIE-9CM, ‘250.53’ if CIE-9CM, ‘250.61’ if CIE-9CM, ‘250.63’ if CIE-9CM, ‘250.71’ if CIE-9CM, ‘250.73’ if CIE-9CM, ‘250.81’ if CIE-9CM, ‘250.83’ if CIE-9CM, ‘250.91’ if CIE-9CM, ‘250.93’ if CIE-9CM or ‘E10’ if CIE-10-ES) during their follow-up or patients with no contact with the health system from 2017-01-01 to 2022-12-31.

### Study period: 
From 2017-01-01 until 2022-12-31.

## IN ORDER TO RUN THE DOCKER FOLLOW THE NEXT STEPS

### 1-HOW TO RUN
Use the following code snippet to create the container.
```bash
docker pull ghcr.io/metodologianavarrabiomed/concept-diabetes:latest

docker run -d -p 127.0.0.1:3000:3000 --name concept-diabetes-aspire ghcr.io/metodologianavarrabiomed/concept-diabetes:latest

```
Open your web browser at http://localhost:3000

### 2-Run the analysis

Follow the steps below.
  1. Map your data in the "MAP DATA" tab.
  2. If everything has worked well, in the "RUN ANALYSIS" tab, select the project "CONCEPT-STROKE" and select the script "**analysis_concept.qmd**"
  3. Go to the "OUTPUTS" tab and download the results.

# Authoring

| Surname, name | Affiliation | ![orcid](https://orcid.org/sites/default/files/images/orcid_16x16.png) ORCID |
|---------------|-------------|------------------------------------------------------------------------------|
| Unidad de Metodología | Navarrabiomed-HUN-UPNA, Instituto de Investigación Sanitaria de Navarra (IdiSNA) | |
| Oscoz-Villanueva, Ignacio | Instituto de Investigación Sanitaria de Navarra (IdiSNA)| https://orcid.org/0009-0004-0387-6056 |
| Tamayo, Ibai | Navarrabiomed-HUN-UPNA | https://orcid.org/0000-0003-2860-3359 |
| Ballesteros-Domínguez, Asier | Instituto de Investigación Sanitaria de Navarra (IdiSNA) | https://orcid.org/0000-0002-2195-4669 |
| Librero, Julián | Navarrabiomed-HUN-UPNA | https://orcid.org/0000-0002-4859-9054 |
| Enguita-Germán, Mónica | Navarrabiomed-HUN-UPNA | https://orcid.org/0000-0002-2890-1252 |
| Ibáñez-Beroiz, Berta | Navarrabiomed-HUN-UPNA | https://orcid.org/0000-0002-7797-4845 |

__Project leader: [Ibáñez-Beroiz, Berta](https://https://orcid.org/0000-0002-7797-4845)__


## How to contribute
- Issue tracker: https://github.com/metodologianavarrabiomed/CONCEPT-DIABETES/issues
- Repository: https://github.com/metodologianavarrabiomed/CONCEPT-DIABETES

## References
- Unidad de Metodología - Evaluación de Servicios Sanitarios: https://navarrabiomed.es/es/servicios/metodologia-evaluacion-de-servicios-sanitarios
- Common Data Model: https://zenodo.org/record/8093865
- Common Data Model Builder library :https://github.com/cienciadedatosysalud/cdmb
- Analytic Software Pipeline Interface for Reproducible Execution (ASPIRE): https://github.com/cienciadedatosysalud/ASPIRE
- Atlas VPM community in Zenodo: https://zenodo.org/communities/atlasvpm
- Research Object Crate (RO-Crate): https://www.researchobject.org/ro-crate/
- ORCID: https://orcid.org
 
<a href="https://creativecommons.org/licenses/by/4.0/" target="_blank" ><img src="https://img.shields.io/badge/license-CC--BY%204.0-lightgrey" alt="License: CC-BY 4.0"></a>
