# Development version of https://github.com/rwdavies/STITCH for use with Nextflow
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM condaforge/mambaforge:4.13.0-1
RUN mamba install -y r-base=4.3.1
RUN Rscript -e 'install.packages("pgenlibr", repos = "http://cran.us.r-project.org")'

LABEL note="Container for https://doi.org/10.1186%2Fs13742-015-0047-8"
LABEL maintainer="saul@ebi.ac.uk"


