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
	\"CategoricalArrays\", \
	\"Flux\", \
	\"MLJ\", \
    \"MLJBase\", \
    \"MLJModelInterface\", \
    \"MLJDecisionTreeInterface\", \
    \"MLJLIBSVMInterface\", \
    \"MLJNaiveBayesInterface\", \
    \"MLJEnsembles\", \
    \"LIBSVM\", \
    \"NearestNeighborModels\", \
    \"DecisionTree\", \
	\"EvoTrees\", \
	\"ScikitLearn\", \
	\"ScikitLearnBase\", \
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
	\"UrlDownload\", \
	\"XGBoost\", \
	\"TSne\", \
]); Pkg.precompile();"

# Pre compile
RUN julia -e "using IJulia,\
                    FileIO,\
                    XLSX,\
                    DelimitedFiles,\
                    CategoricalArrays,\
                    Flux,\
                    MLJ, \
                    MLJBase, \
                    MLJModelInterface, \
                    MLJDecisionTreeInterface, \
                    MLJLIBSVMInterface, \
                    MLJNaiveBayesInterface, \
                    MLJEnsembles, \
                    LIBSVM, \
                    NearestNeighborModels, \
                    DecisionTree, \
                    EvoTrees, \
                    ScikitLearn,\
                    ScikitLearnBase,\
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
                    UrlDownload,\
                    XGBoost,\
                    TSne\
                    ;"

RUN chown -R $NB_UID:$NB_GID /home/jovyan

USER $NB_UID
