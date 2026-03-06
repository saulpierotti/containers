# General-purpose container with data.table and tidyverse in R
# Author: Saul Pierotti
# Mail: saulpierotti@gmail.com

FROM condaforge/mambaforge:24.9.2-0

RUN mamba install --yes \
	r-base=4.5.2 \
	r-tidyverse=2.0.0 \
	r-data.table=1.17.8 \
	r-r.utils=2.13.0

LABEL note="General-purpose container with data.table and tidyverse in R"
LABEL maintainer="saulpierotti@gmail.com"
