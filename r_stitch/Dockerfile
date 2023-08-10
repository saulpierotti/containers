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
	rsync \
	&& \
	apk add -X http://dl-cdn.alpinelinux.org/alpine/edge/testing htslib-tools \
	&& \
	rm -rf /var/cache/apk/*

RUN git clone \
	--recursive \
	--depth 1 \
	https://github.com/rwdavies/STITCH.git \
	--branch 1.6.10 \
	&& \
	STITCH/scripts/install-dependencies.sh \
	&& \
	wget https://github.com/rwdavies/stitch/releases/download/1.6.10/STITCH_1.6.10.tar.gz \
	&& \
	R CMD INSTALL STITCH_1.6.10.tar.gz \
	&& \
	rm -rf STITCH STITCH_1.6.10.tar.gz

LABEL note="Container for https://github.com/rwdavies/STITCH"
LABEL maintainer="saul@ebi.ac.uk"


