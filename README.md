
![GitHub](https://img.shields.io/github/license/ennanco/MIA_ML1?style=flat-square) ![Julia](https://img.shields.io/badge/Julia-1.7.2-blueviolet?logo=Julia)

# Machine Learning I

![Banner](img/MLI.png)

This repository hosts the initial exercises for the subject **Machine Learning I** in the Master in Artificial Intelligence, which is jointly offered by the three Galician universities: the University of A Coruña (UDC), the University of Santiago de Compostela (USC), and the University of Vigo (UVigo).

The notebooks in this repository are based on the initial work of Daniel Rivero Cebrián, a former instructor of the subject, who generously provided materials to support the current development.

The practical sessions will be conducted using [Julia](https://julialang.org/), a widely used language in machine learning research. These exercises have been tested on Julia version 1.7.2, though they should also be compatible with versions starting from 1.2.0.


# Teaching Staff:
* **Enrique Fernández Blanco** (Course Coordinator, UDC)
* **Víctor M. Darriba Bilbao** (UVigo)
* **Nelly Condori Fernández** (USC)


# Docker Environment

A Docker image has been prepared with all necessary libraries and configurations. It’s based on the Jupyter Docker image and includes:

- **Jupyter Lab** = 4.0.5
- **Julia** = 1.9.3

| Julia Library      | Version |
|--------------------|:-------:|
| CSV                | 0.10.11 |
| DataFrames         | 1.6.1   |
| DelimitedFiles     | 1.9.1   |
| FileIO             | 1.16.1  |
| Flux               | 0.14.5  |
| IJulia             | 1.24.2  |
| Images             | 0.26.0  |
| JLD2               | 0.4.33  |
| MAT                | 0.10.5  |
| Plots              | 1.39.0  |
| Pluto              | 0.19.27 |
| ScikitLearn        | 0.7.0   |
| StatsPlots         | 0.15.6  |
| Tables             | 1.10.1  |
| XLSX               | 0.10.0  |
| Statistics         | 1.9.0   |

- **Python** = 3.11.2

| Python Library     | Version |
|--------------------|:-------:|
| IPyKernel          | 6.25.1  |
| jupyter-pluto-proxy| 0.1.2   |
| Matplotlib         | 3.7.2   |
| Numpy              | 1.25.2  |
| Pandas             | 2.1.0   |
| Plotly             | 5.16.1  |
| rich               | 13.5.2  |
| seaborn            | 0.12.2  |


## Docker Setup Options

There are two ways to set up the Docker environment:

### 1. Build from Scratch
If you have cloned the repository, build the Docker image using the following command:

```bash
    docker built -t ennanco/machinelearning1 docker/

```

This build process takes approximately 15 minutes.

## Pull from Docker Hub
Alternatively, you can download the pre-built image from Docker Hub:

```bash
    docker pull ennanco/machinelearning1

```

The download size is around 2 GB, so the time required will depend on your internet speed.

## Running the Environment
To start the Docker environment, navigate to the cloned folder and run:
```bash
    docker run -p 8888:8888 -v ${PWD}/.:/home/jovyan/work ennanco/machinelearning1

```
This command will open a Jupyter Lab environment in your browser, pre-configured with all necessary libraries for the subject.


