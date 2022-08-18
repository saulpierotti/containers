# This container image includes a functioning installation of idtrackerai,
# scientific software used for tracking of the movement of animals in videos
# obtained in laboratory conditions. This version includes the GUI version of
# idtrackerai running on GPU. It cannot run without a GPU in the system.
# The application can be also run from the terminal without a graphical
# environment. This version has been tweaked so to set the paramter
# `allowgrowth` to True for tensorflow. This avoids fails due to multiple
# processs running on the same GPU, but can degrade performances.

# This is not an official distribution and it was developped independently from
# the idtrackerai authors. All the credit for idtrackerai to its original
# authors.
#
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: February 11th 2022

# NOTE: if the following image is unavailable it can be built
# from workflow/envs/idtrackerai_gpu_gui/Dockerfile
FROM saulpierottiebi/idtrackerai_gpu_gui:latest

COPY ./cnn_utils.py /opt/conda/lib/python3.6/site-packages/idtrackerai/utils/cnn_utils.py

LABEL note="\
Refer to the container image saulpierottiebi/idtrackerai_gpu_gui for all the notes and testing \
procedures.\
This version has been patched so that tensorflow works with the paramter allowgrowth=true. \
This means that it reserves a minimal amount of VRAM which is then expanded, instead of reserving the whole VRAM at the beginning. \
This prevent some crashes when concurrent processes are running on the same GPU, but may degrade performances.\
"

LABEL maintainer="saul@ebi.ac.uk"


