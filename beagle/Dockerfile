# Development version of https://github.com/rwdavies/STITCH for use with Nextflow
# Author: Saul Pierotti
# Mail: saul@ebi.ac.uk

# Corretto is a no-cost, production-ready distribution of the Open Java Development Kit (OpenJDK).
FROM amazoncorretto

# needed by nextflow
RUN yum install -y procps
RUN curl http://faculty.washington.edu/browning/beagle/beagle.22Jul22.46e.jar --output /usr/bin/beagle.jar

LABEL note="Execute beagle with java -jar /usr/bin/beagle.jar"
LABEL maintainer="saul@ebi.ac.uk"
