# Dockerfiles

## Descritpion

Set of dockerfiles for basic development in some languages

Latest Avaliable:

### Basic Python3 Template
Contents: numpy scipy matploblib Iptyhon seaborn pandas jupyter

### Python3 for Audio Processing
Contents: numpy scipy matplotlib pymir3 sklearn IPython cython seaborn pandas jupyter

### Python3 (Anaconda) to Audio Signal Processing for Machine Learning
Contents: Anaconda distribution and librosa.
Setup for following the "Audio Signal Processing for Machine Learning"
Video Series from Valerio Velardo YouTube Channel (The Sound of AI)

### Python3 for Basic Image processing
Contents: numpy scipy matplotlib scikit-image pillow openCV seaborn pandas jupyter 

### Python3 for Advanced Image processing (TODO)
Contents:

## Building the Dockerfiles:

 1) ```docker build . ```
 2) ```docker run -it -p 8888:8888 -v $[WORKSPACE PATH]:/home/Documents/WORKDIR <generated img ID> /bin/bash ```
    Example: ```docker run -it -p 8888:8888 -v $(pwd)/workspace:/home/Documents/WORKDIR 1a12fd2478a9 /bin/bash```

 3) inside docker container, use ``` jupyter notebook --ip=* --allow-root``` to run jupyter notebook. 
    since no browser is installed, you can click on the generated URL to  start running jupyter notebook.```



