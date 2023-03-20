# Mambaforge container with pomegranate installed from pip

# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: August 18th 2022

FROM condaforge/mambaforge:4.13.0-1

RUN mamba install -c conda-forge python=3.10.5 pandas=1.4.3 numpy=1.23.1 \
    scikit-learn=1.1.1 pip=22.2.2 scipy=1.8.1 h5py=3.7.0
RUN mamba install -c conda-forge gcc=12.1.0
RUN mamba install -c conda-forge matplotlib=3.5.3
RUN mamba install -c conda-forge h5py=3.7.0

# GPU support
RUN mamba install -c conda-forge cupy=11.3.0 

# needed for nice HMM plots
RUN mamba install -c conda-forge pygraphviz=1.9

# use my fork of pomegranate
RUN mamba install -c conda-forge cython=0.29.32
RUN git clone https://github.com/saulpierotti-ebi/pomegranate.git
RUN cd pomegranate && \
    git checkout 2d8ff0a049076960f8b6d593fca88964443f613b && \
    python setup.py install

LABEL note="\
Mambaforge container with pomegranate installed from pip"

LABEL maintainer="saul@ebi.ac.uk"
