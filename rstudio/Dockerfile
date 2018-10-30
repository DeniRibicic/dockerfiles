FROM rocker/rstudio
MAINTAINER "Deni Ribicic" <dribicic@gmail.com>

#install cran-R packages
RUN install2.r --error \
    -r "https://cran.rstudio.com" \
    -r "http://www.bioconductor.org/packages/release/bioc" \
    reshape2 \
    vegan
    
# Clean
RUN apt-get clean \
  && rm -rf /tmp/downloaded_packages/* \
  && rm -rf /var/lib/apt/lists/*
