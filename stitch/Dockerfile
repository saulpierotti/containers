# Development version of https://github.com/rwdavies/STITCH for use with Nextflow
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM alpine:3.18.2

#RUN apk update
run apk add git
RUN git clone --recursive https://github.com/rwdavies/STITCH.git
RUN apk add bash
RUN apk add R
RUN apk add alpine-sdk
RUN apk add R-dev
RUN apk add linux-headers
RUN apk add libxml2-dev
RUN apk add libpng-dev
RUN apk add tiff-dev
RUN apk add libjpeg-turbo-dev
RUN apk add freetype-dev
RUN apk add libgit2-dev
RUN apk add fontconfig-dev
RUN apk add pandoc
RUN apk add fribidi-dev
RUN apk add harfbuzz-dev
RUN STITCH/scripts/install-dependencies.sh
RUN wget https://github.com/rwdavies/stitch/releases/download/1.6.10/STITCH_1.6.10.tar.gz
RUN apk add autoconf
RUN apk add automake
RUN R CMD INSTALL STITCH_1.6.10.tar.gz
RUN apk add rsync

LABEL note="Container for https://github.com/rwdavies/STITCH for use with Nextflow"
LABEL maintainer="saul@ebi.ac.uk"


