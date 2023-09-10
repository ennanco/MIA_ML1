
![GitHub](https://img.shields.io/github/license/ennanco/MIA_ML1?style=flat-square) ![Julia](https://img.shields.io/badge/Julia-1.7.2-blueviolet?logo=Julia)

![Banner](img/MLI.png)

This repository contains the initial exercises that are going to be covered in the subject Machine Learning I of the Master in Artificial Intelligence taught at the three universities of Galicia, i.e., University of A Coruña (UDC), University of Santiago de Compostela (USC), University of Vigo (UVigo).

The practical part of the subject is going to be taught in [Julia](https://julialang.org/) which is a common language in the research with Machine Learning. These exercises have been tested with version 1.7.2, however, the previous version should also work since version 1.2.0.


# Teaching Staff:
* Daniel Rivero Cebrián (responsable, UDC)
* Víctor M. Darriba Bilbao (UVigo)
* Enrique Fernández Blanco (UDC)
* Lara M. Vázquez González (USC)
* Nelly Condori Fernández (USC)



# Docker version

There is a docker prepared with the libraries and the system alredy setup. To run it, you would need docker setup. It is based on the image create by the Jupyter development team. It contains the following:
* Jupyter Lab
* Julia
    * IJulia
    * \"FileIO\", \
    * \"XLSX\", \
    * JLD2
    * DelimitedFiles
    * CSV
    * Flux
    * ScikitLearn
    * Plots
    * MAT
    * Tables
    * Images
    * DataFrames
    * Statistics
    * StatsPlots
* Pluto.jl
* Python
    * Matplotly
    * Plotly
    * rich
    * seaborn


There are two posibilities:

## Build from scratch
Execute the building process from the Dockerfile in docker, if you have clone the repository:

> docker built -t ennanco/machinelearning1 docker/.

This command would take about 15 minutes to execute and create the image.

## Pull from Docker Hub repository
Execute the following command:

>docker pull ennanco/machinelearning1

In this case, the download size is about 2GBytes, so it is going to be quite dependant on your connection.

## Run the practice environment

To run the docker environment, you should execute the following command in the cloned folder:

>  docker run -p 8888:8888 -v ${PWD}/.:/home/jovyan/work ennanco/machinelearning1

This should pop up the browser with a Jupyter Lab environment and the libraries required for this subject already setup



