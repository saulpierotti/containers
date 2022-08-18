# Mambaforge container with pomegranate installed from pip

# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: August 18th 2022

FROM condaforge/mambaforge:4.13.0-1

RUN mamba install -c conda-forge python=3.10.5 pandas=1.4.3 numpy=1.23.1 \
    scikit-learn=1.1.1 pip=22.2.2 scipy=1.8.1 h5py=3.7.0

RUN mamba install -c conda-forge gcc=12.1.0

RUN pip3 install pomegranate==0.14.8

LABEL note="\
Mambaforge container with pomegranate installed from pip"

LABEL maintainer="saul@ebi.ac.uk"
