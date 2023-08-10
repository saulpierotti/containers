# General-purpose containers with tools for out-of-core genomics data analisis in python
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM condaforge/mambaforge:23.1.0-4

RUN mamba install --yes -c conda-forge \
	python=3.10.12 \
	anndata=0.9.1 \
	dask=2023.6.1 \
	zarr=2.15.0 \
	scikit-allel=1.3.6 \
	zlib=1.2.13 \
	bioconda::tabix=1.11

ENTRYPOINT "/bin/bash"

LABEL note="General-purpose containers with tools for out-of-core genomics data analysis in python"
LABEL maintainer="saul@ebi.ac.uk"
