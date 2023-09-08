# Development version of https://github.com/rwdavies/STITCH for use with Nextflow
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

FROM alpine:3.18.2

RUN apk update && apk add \
	git \
	bash \
	R \
	alpine-sdk \
	R-dev \
	linux-headers \
	libxml2-dev \
	libpng-dev \
	tiff-dev \
	libjpeg-turbo-dev \
	freetype-dev \
	libgit2-dev \
	fontconfig-dev \
	pandoc \
	fribidi-dev \
	harfbuzz-dev \
	autoconf \
	automake \
	&& \
	apk add -X http://dl-cdn.alpinelinux.org/alpine/edge/testing htslib-tools \
	&& \
	rm -rf /var/cache/apk/*

RUN Rscript -e 'install.packages("pgenlibr", repos = "http://cran.us.r-project.org")'

LABEL note="Container for https://doi.org/10.1186%2Fs13742-015-0047-8"
LABEL maintainer="saul@ebi.ac.uk"


