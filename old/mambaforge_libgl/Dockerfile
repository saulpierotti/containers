# Mambaforge container with added the libgl library, needed for using opencv

# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: February 14th 2022

FROM condaforge/mambaforge:4.11.0-2

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install libgl1-mesa-glx -y

LABEL note="\
Mambaforge container with added the libgl library, needed for using opencv"

LABEL maintainer="saul@ebi.ac.uk"
