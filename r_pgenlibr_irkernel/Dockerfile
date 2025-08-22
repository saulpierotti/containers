FROM ubuntu:25.10
RUN apt update && apt install -y build-essential r-base && rm -rf /var/lib/apt/lists/*
RUN R -e 'install.packages("pgenlibr")'
RUN R -e 'install.packages("IRkernel")'
RUN R -e 'install.packages("data.table")'
RUN R -e 'install.packages("r.utils")'
RUN R -e 'install.packages("tidyverse")'


