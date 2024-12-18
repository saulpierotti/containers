# Development version of https://github.com/rwdavies/STITCH for use with Nextflow
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM condaforge/mambaforge:23.1.0-1

RUN mamba install -c conda-forge r-base=4.2.3 r-tidyverse=2.0.0 r-data.table=1.14.8
RUN R -e "install.packages('BiocManager', repos = 'http://cran.us.r-project.org')"
RUN R -e "BiocManager::install(version = '3.16')"

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update -y && apt install -y build-essential libxml2

RUN R -e "BiocManager::install('biomaRt')"

LABEL note="biomaRt installation from bioconductors with tidyverse and data.table"
LABEL maintainer="saul@ebi.ac.uk"
