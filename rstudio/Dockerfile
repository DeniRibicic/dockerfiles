FROM rocker/rstudio
MAINTAINER "Deni Ribicic" <dribicic@gmail.com>

#install cran-R packages
RUN Rscript -e "install.packages('vegan')"

# Clean
RUN apt-get clean \
  && rm -rf /tmp/downloaded_packages/* \
  && rm -rf /var/lib/apt/lists/*
