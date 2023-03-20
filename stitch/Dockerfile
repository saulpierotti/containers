# Development version of https://github.com/rwdavies/STITCH for use with Nextflow
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM condaforge/mambaforge:22.11.1-4

ENV DEBIAN_FRONTEND=noninteractive

RUN mamba install -c conda-forge r-base=4.2.3
RUN mamba install -c bioconda r-rrbgen=0.0.6
RUN mamba install -c conda-forge r-remotes=2.4.2
RUN apt update && apt upgrade -y
RUN apt install -y apt-utils
RUN apt install -y pkg-config
RUN apt install -y autoconf
RUN apt install -y automake
RUN apt install -y xz-utils
RUN apt install -y zlib1g-dev
RUN apt install -y libbz2-dev
RUN apt install -y liblzma-dev
RUN apt install -y build-essential
RUN Rscript -e "remotes::install_github(\"rwdavies/STITCH/STITCH\")"
RUN apt install -y rsync
RUN mamba install -c bioconda htslib=1.17

LABEL note="Development version of https://github.com/rwdavies/STITCH for use with Nextflow"
LABEL maintainer="saul@ebi.ac.uk"


