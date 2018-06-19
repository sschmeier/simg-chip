Bootstrap: docker
From: continuumio/miniconda3:4.5.4

%labels
   AUTHOR schmeier@tuta.io

%environment
# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# This sets global environment variables for anything run within the container
  export PATH="/opt/conda/bin:/usr/local/bin:/usr/bin:/bin:"
  unset CONDA_DEFAULT_ENV
  export ANACONDA_HOME=/opt/conda


%post
   export PATH=/opt/conda/bin:$PATH
   echo "We add conda channels and install tools."
   conda config --add channels defaults
   conda config --add channels conda-forge
   conda config --add channels bioconda
   conda install --yes colorama=0.3.9
   conda install --yes snakemake=5.1.4
   conda install --yes bedtools=2.27.1
   conda install --yes scipy=1.1
   conda clean --index-cache --tarballs --packages --yes