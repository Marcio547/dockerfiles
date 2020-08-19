# HOW TO BUILD

# 1) docker build .
# 2) docker run -it -p 8888:8888 -v $[WORKSPACE PATH]:/home/Documents/WORKDIR <generated img ID> /bin/bash
# Example: docker run -it -p 8888:8888 -v $(pwd)/workspace:/home/Documents/WORKDIR 1a12fd2478a9 /bin/bash

# 3) inside docker container, use jupyter notebook --ip=* --allow-root to run jupyter notebook. 
#    since no browser is installed, you can click on the generated URL to  start running jupyter notebook.

FROM ubuntu:18.04 

RUN echo "Audio Processing Tools Container"

## python installation
RUN apt-get update && apt-get install -y git \ 
                python3 \
                python3-pip \
                python3-setuptools 

## python libraries for Audio processing
RUN pip3 install numpy scipy matplotlib pymir3 sklearn IPython cython seaborn pandas jupyter

RUN apt-get install vim -y

## Auxiliary folders for mounting worskpace and downloading auxiliary repos
RUN mkdir -p /home/Documents/WORKDIR
RUN mkdir -p /home/Documents/REPOS
