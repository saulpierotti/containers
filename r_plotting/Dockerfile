# This is a container that includes all the dependencies that I need for creating plots with R
#
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: May 17th 2022

FROM condaforge/mambaforge:4.12.0-0

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update -y &&\
    apt install -y texlive-full

RUN mamba install -c conda-forge \
	r-base=4.1.3 \
	r-tidyverse=1.3.1 \
	r-cowplot=1.1.1 \
	r-ggthemes=4.2.4 \
	r-ggpubr=0.4.0 \
	r-r.utils=2.11.0

RUN Rscript -e "install.packages('tikzDevice', repos='https://cloud.r-project.org/')"

LABEL note="\
This is a container that includes all the dependencies that I need for creating plots with R \
"

LABEL maintainer="saul@ebi.ac.uk"


