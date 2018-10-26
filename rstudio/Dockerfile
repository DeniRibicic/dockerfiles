FROM rocker/rstudio
MAINTAINER "Deni Ribicic" <dribicic@gmail.com>

# Install bioconductor packages
RUN Rscript -e "source('http://bioconductor.org/biocLite.R');biocLite('phyloseq')"

#install cran-R packages
RUN Rscript -e "install.packages('vegan')"

# Clean
RUN apt-get clean \
  && rm -rf /tmp/downloaded_packages/* \
  && rm -rf /var/lib/apt/lists/*
