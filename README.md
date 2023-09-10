
![GitHub](https://img.shields.io/github/license/ennanco/MIA_ML1?style=flat-square) ![Julia](https://img.shields.io/badge/Julia-1.7.2-blueviolet?logo=Julia)

![Banner](img/MLI.png)

This repository contains the initial exercises that are going to be covered in the subject Machine Learning I of the Master in Artificial Intelligence taught at the three universities of Galicia, i.e., University of A Coruña (UDC), University of Santiago de Compostela (USC), University of Vigo (UVigo).

The practical part of the subject is going to be taught in [Julia](https://julialang.org/) which is a common language in the research with Machine Learning. These exercises have been tested with version 1.7.2, however, the previous version should also work since version 1.2.0.


# Teaching Staff:
* Daniel Rivero Cebrián (responsable, UDC)
* Víctor M. Darriba Bilbao (UVigo)
* Enrique Fernández Blanco (UDC)
* Nelly Condori Fernández (USC)



# Docker version

There is a docker prepared with the libraries and the system alredy setup. To run it, you would need docker setup. It is based on the image create by the Jupyter development team. It contains the following:
* Jupyter Lab = 4.0.5
* Julia = 1.9.3

| Resource    | Version |
|-------------|:---------:|
| CSV          | 0.10.11 |
| DataFrames  | 1.6.1   |
| DelimitedFiles | 1.9.1 |
| FileIO      | 1.16.1  |
| Flux        | 0.14.5  |
| IJulia      | 1.24.2  |
| Images      | 0.26.0  |
| JLD2        | 0.4.33  |
| MAT         | 0.10.5  |
| Plots       | 1.39.0  |
| Pluto       | 0.19.27 |
| ScikitLearn | 0.7.0   |
| StatsPlots  | 0.15.6  |
| Tables      | 1.10.1  |
| XLSX        | 0.10.0  |
| Statistics  | 1.9.0   |

* Python = 3.11.2

| Resource    | Version |
|-------------|:---------:|
| IPyKernel   | 6.25.1  |
| jupyter-pluto-proxy| 0.1.2 |
| Matplotlib  | 3.7.2   |
| Numpy       | 1.25.2  |
| Pandas      | 2.1.0   |
| Plotly      | 5.16.1  |
| rich        | 13.5.2  |
| seaborn     | 0.12.2  |


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



