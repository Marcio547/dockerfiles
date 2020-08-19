# HOW TO BUILD

# 1) docker build .
# 2) docker run -it -p 8888:8888 -v $[WORKSPACE PATH]:/home/Documents/WORKDIR <generated img ID> /bin/bash
# Example: docker run -it -p 8888:8888 -v $(pwd)/workspace:/home/Documents/WORKDIR 1a12fd2478a9 /bin/bash

# 3) inside docker container, use jupyter notebook --ip=* --allow-root to run jupyter notebook. 
#    since no browser is installed, you can click on the generated URL to  start running jupyter notebook.

FROM continuumio/anaconda3 

RUN echo "Audio Signal Processing for Machine Learning Container"

## git installation
RUN apt-get update && apt-get install -y git  

#anaconda update and librosa installation
RUN conda update conda

RUN conda update anaconda

RUN conda install -c conda-forge librosa

#vim installation
RUN apt-get install vim -y

## Auxiliary folders for mounting worskpace and downloading auxiliary repos
RUN mkdir -p /home/Documents/WORKDIR
RUN mkdir -p /home/Documents/REPOS


# Clone Repo for Audio Signal Processing for Machine Learning, from Valerio Velardo's Github:
RUN git clone https://github.com/musikalkemist/AudioSignalProcessingForML.git /home/Documents/REPOS/AudioProcessingForML
