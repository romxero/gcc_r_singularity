Bootstrap: docker
From: gcc:9.2

%labels
Author "Randall Cab White - rcwhite@stanford.edu"


#########
#%setup
#########

#Downlaod packages
%post
  apt-get -ym update
  apt-get -ym install wget libatlas3-base curl make tar gzip default-jdk default-jre
  cd /
  wget https://cran.r-project.org/src/base/R-3/R-3.6.1.tar.gz
  tar zxvf R-3.6.1.tar.gz
  cd R*
  ./configure
  make -j3
  make install
%environment
  export IMAGE_NAME="gcc"
#%runscript
#	/firefox/firefox-bin


