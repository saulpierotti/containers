# This container image includes a functioning installation of idtrackerai,
# scientific software used for tracking of the movement of animals in videos
# obtained in laboratory conditions. This version includes the CLI version of
# idtrackerai running on GPU.

# This is not an official distribution and it was developped independently from
# the idtrackerai authors. All the credit for idtrackerai to its original
# authors. Visit the idtrackerai website for more information:
#
# https://idtrackerai.readthedocs.io/en/latest/
#
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: September 22th 2022
#
# Idtrackerai credits:
#
# Romero-Ferrero, F., Bergomi, M.G., Hinz, R.C., Heras, F.J.H., de Polavieja, G.G., Nature Methods, 2019. idtracker.ai: tracking all individuals in small or large collectives of unmarked animals.
# (F.R.-F. and M.G.B. contributed equally to this work. Correspondence should be addressed to G.G.d.P: gonzalo.polavieja@neuro.fchampalimaud.org)

FROM condaforge/mambaforge:latest

RUN mamba install python=3.7
RUN mamba install pytorch torchvision -c pytorch
ENV DEBIAN_FRONTEND=noninteractive
RUN apt update -y
RUN apt install -y locales &&\
    echo "LC_ALL=en_US.UTF-8" >> /etc/environment &&\
    echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen &&\
    echo "LANG=en_US.UTF-8" > /etc/locale.conf &&\
    locale-gen en_US.UTF-8
RUN /opt/conda/bin/pip install 'idtrackerai[cli]==4.0.9'
RUN chmod +w /opt/conda/lib/python3.7/site-packages/idtrackerai

ENTRYPOINT bash

LABEL note="\
This is not an official container for idtrackerai.\
Absolutely no warranty implied, use at your own risk.\
Credit to the original authors of idtrackerai.\
"
LABEL maintainer="saul@ebi.ac.uk"


