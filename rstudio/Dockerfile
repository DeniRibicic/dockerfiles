FROM rocker/rstudio:3.4.3
MAINTAINER "Deni Ribicic" <dribicic@gmail.com>

# Install bioconductor packages
RUN Rscript -e "source('http://bioconductor.org/biocLite.R')"
RUN Rscript -e "biocLite('phyloseq')"

#install cran-R packages
RUN Rscript -e "install.packages('vegan')"

# Clean
RUN apt-get clean \
  && rm -rf /tmp/downloaded_packages/* \
  && rm -rf /var/lib/apt/lists/*
