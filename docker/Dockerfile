FROM jupyter/julia-notebook
LABEL author="Enrique Fernández Blanco"


USER root
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update &&\
    apt-get install -y htop &&\
    pip install matplotlib plotly rich seaborn

# ========== Install Julia packages as application user ==========

RUN julia -e "using Pkg; Pkg.add.([ \
	\"IJulia\", \
	\"FileIO\", \
	\"XLSX\", \
	\"JLD2\", \
	\"DelimitedFiles\", \
	\"CSV\", \
	\"Flux\", \
	\"MLJ\", \
    \"LIBSVM\", \
    \"NearestNeighborModels\", \
    \"DecisionTree\", \
	\"ScikitLearn\", \
	\"Plots\", \
	\"MAT\", \
	\"Tables\", \
	\"Images\", \
	\"DataFrames\", \
	\"Statistics\", \
	\"StatsPlots\", \
	\"MultivariateStats\", \
	\"NaiveBayes\", \
	\"MLJLinearModels\", \
	\"TSne\", \
]); Pkg.update;"

# Pre compile
RUN julia -e "using IJulia,\
                    FileIO,\
                    XLSX,\
                    DelimitedFiles,\
                    Flux,\
                    MLJ, \
                    LIBSVM, \
                    NearestNeighborModels, \
                    DecisionTree, \
                    ScikitLearn,\
                    Plots,\
                    MAT,\
                    Tables,\
                    Images,\
                    DataFrames,\
                    Statistics,\
                    StatsPlots,\
                    MultivariateStats,\
                    NaiveBayes,\
                    MLJLinearModels,\
                    TSne\
                    ;"
RUN chown -R $NB_UID:$NB_GID /home/jovyan

USER $NB_UID
