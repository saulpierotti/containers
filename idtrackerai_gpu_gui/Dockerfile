# syntax=docker/dockerfile:1

# This container image includes a functioning installation of idtrackerai,
# scientific software used for tracking of the movement of animals in videos
# obtained in laboratory conditions. This version includes the GUI version of
# idtrackerai running on GPU. It cannot run without a GPU in the system.
# The application can be also run from the terminal without a graphical
# environment.

# This is not an official distribution and it was developped independently from
# the idtrackerai authors. All the credit for idtrackerai to its original
# authors.
#
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk
# Edited: February 11th 2022

# NOTE: if the following image is unavailable it can be built
# from workflow/envs/idtrackerai_cpu_gui/Dockerfile
FROM saulpierottiebi/idtrackerai_cpu_gui:latest

RUN conda install tensorflow-gpu=1.13

LABEL note="\
Refer to the container image saulpierottiebi/idtrackerai_cpu_gui for all the notes and testing \
procedures.\
IMPORTANT: Tensorflow 1.13 allocates the whole VRAM on execution. If other processes are running on the same GPU and using VRAM \
idtrackerai_test fails with ethe following error:\
\
'Failed to get convolution algorithm. This is probably because cuDNN failed to initialize, so try looking to see if a warning log message was printed above.'\
\
With Spectre-LSF, this can be solved by specifying --gpu 'num=1,mode=exclusive_process'\
"

LABEL maintainer="saul@ebi.ac.uk"


