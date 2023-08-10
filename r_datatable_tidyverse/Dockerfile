# General-purpose container with data.table and tidyverse in R
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM condaforge/mambaforge:23.1.0-4

RUN mamba install --yes \
	r-base=4.3.1 \
	r-tidyverse=2.0.0 \
	r-data.table=1.14.8 \
	r-r.utils=2.12.2

LABEL note="General-purpose container with data.table and tidyverse in R"
LABEL maintainer="saul@ebi.ac.uk"
