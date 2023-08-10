# This is a container that includes all the dependencies that I need for creating plots with R
#
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM condaforge/mambaforge:23.1.0-4

RUN mamba install --yes r-base=4.3.1 r-tidyverse=2.0.0 r-cowplot=1.1.1 r-ggthemes=4.2.4 r-ggpubr=0.6.0 r-r.utils=2.12.2
RUN Rscript -e "install.packages('tikzDevice', repos='https://cloud.r-project.org/')"

LABEL note="This is a container that includes all the dependencies that I need for creating plots with R"

LABEL maintainer="saul@ebi.ac.uk"


