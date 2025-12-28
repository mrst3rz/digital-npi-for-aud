<a href="https://doi.org/10.5281/zenodo.17206606"><img src="https://zenodo.org/badge/1018696552.svg" alt="DOI"/></a>

# Reproducible R Analyses of Digital Neuropsychological Interventions for Alcohol Use Disorder

## Overview

This repository contains the complete reproducible analysis workflow for a systematic review and meta-analysis examining the clinical effectiveness of digital neuropsychological interventions targeting alcohol use disorder (AUD).

The repository includes all R-based analysis scripts, bibliographic resources, and environment specifications required to reproduce the reported results or to update the analyses as new evidence becomes available.

## Repository contents

-   `Meta-Analysis of Neuropsychological Interventions.Rmd`\
    Primary R Markdown document containing data preparation, statistical analyses, and manuscript text.

-   `renv.lock`\
    File specifying the exact versions of R packages used in the analyses.

-   `renv/`\
    Files required to restore the project-specific R library using the `renv` package.

-   `references.yaml`, `grateful-refs.bib`\
    Bibliographic metadata for cited literature and R package citations.

## Software requirements

The analyses require the following software:

-   R (version ≥ 4.2)
-   RStudio (recommended)
-   Pandoc (installed automatically with RStudio)

## Reproducibility instructions

To reproduce the analyses and regenerate all results reported in the manuscript, please follow these steps:

1.  Clone the repository:

    ``` bash
    git clone https://github.com/mrst3rz/digital-npi-for-aud.git
    cd digital-npi-for-aud
    ```

2.  Restore the R package environment:

    ``` bash
    renv::restore()
    ```

3.  Render the R Markdown document:

    ``` bash
    rmarkdown::render("Meta-Analysis of Neuropsychological Interventions.Rmd")
    ```

## Data availability

The data used in the analyses are not stored directly in this repository.
Instead, the workflow retrieves the required data sets programmatically from the Open Science Framework (OSF).

Access to the data requires appropriate authorization and an OSF personal access token.
Users with permission can reproduce the analyses by supplying their own OSF token as an environment variable prior to execution of the workflow.

The data set used for the published meta-analysis can be made available upon request.

### OSF authentication

To enable programmatic access to OSF, set an OSF personal access token in your R session (do not commit the token):

``` r
Sys.setenv(OSF_TOKEN = "your_personal_access_token")
```

## Affiliation

This work was conducted in affiliation with the University of Southern Denmark.

## Citation

If this code or workflow is used, please cite the corresponding manuscript and the archived version of this repository (doi.org/10.5281/zenodo.17206606), when applicable.

## License

This repository is distributed under the MIT License.

[MIT](https://choosealicense.com/licenses/mit/)
