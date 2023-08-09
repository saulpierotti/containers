# General-purpose containers with tools for out-of-core genomics data analisis in python
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

# Corretto is a no-cost, production-ready distribution of the Open Java Development Kit (OpenJDK).
FROM condaforge/mambaforge:23.1.0-4

# needed by nextflow
RUN mamba install --yes python=3.10.12 anndata=0.9.1 dask=2023.6.1 zarr=2.15.0 scikit-allel=1.3.6 bioconda::tabix=1.11

ENTRYPOINT "/bin/bash"

LABEL note="General-purpose containers with tools for out-of-core genomics data analisis in python"
LABEL maintainer="saul@ebi.ac.uk"
