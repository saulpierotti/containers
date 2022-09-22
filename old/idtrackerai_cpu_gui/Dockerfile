# This container image includes a functioning installation of idtrackerai,
# scientific software used for tracking of the movement of animals in videos
# obtained in laboratory conditions. This version includes the GUI version of
# idtrackerai running on CPU. No GPU support is included. The application can
# be also run from the terminal without a graphical environment.

# This is not an official distribution and it was developped independently from
# the idtrackerai authors. All the credit for idtrackerai to its original
# authors.
#
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: February 11th 2022

FROM condaforge/mambaforge:latest


RUN mamba install python=3.7 pip
RUN pip3 install "idtrackerai[gui]"

ENV DEBIAN_FRONTEND=noninteractive
RUN apt update -y &&\
    apt install -y locales &&\
    echo "LC_ALL=en_US.UTF-8" >> /etc/environment &&\
    echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen &&\
    echo "LANG=en_US.UTF-8" > /etc/locale.conf &&\
    locale-gen en_US.UTF-8 &&\
    apt install -y qtbase5-dev
RUN mamba install pytorch torchvision -c pytorch

ENTRYPOINT idtrackerai

LABEL note="\
This is not an official container for idtrackerai. \
This countainer can only be run with singularity (required for the GUI). \
Absolutely no warranty implied, use at your own risk.\
"
LABEL how.to.test="\
Open a shell in the container using singularity \'run --writable-tmpfs\' and run \
\'idtrackerai_test -o [output_dir]\'. Note that the output directory must be specified \
otherwise idtrackerai_test tries to write on its own directory in /opt and fails since \
there is not enough space. The \'--writable-tmpfs\' flag is also required since \
idtrackerai_test also edits some small files in its own directory in /opt even when the \
output directory is set.\
"
LABEL maintainer="saul@ebi.ac.uk"


