# reproducibility-tutorial
FOSS 2020
    1  cd /scratch
    2  df -h
    3  git clone https://github.com/slittin/reproducibility-tutorial.git
    4  ls
    5  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    6  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    7  ln -s /opt/conda/pkgs/*/bin/* /bin
    8  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
    9  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   10  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   11  /opt/conda/bin/pip install bash_kernel
   12  /opt/conda/bin/pip install ipykernel
   13  /opt/conda/bin/python3 -m bash_kernel.install
   14  /opt/conda/bin/conda search htseq
   15  /opt/conda/bin/conda search -c bioconda htseq
   16  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   17  clear
   18  /opt/conda/bin/conda search -c bioconda snakemake
   19  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   20  ln -s /opt/conda/bin/* /bin
   21  ln -s /opt/conda/lib/* /usr/lib
   22  snakemake --version
   23  sudo apt-get update
   24  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   25  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   26  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   27  sudo apt-get update
   28  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   29  docker run hello-world
   30  cd /scratch/reproducibility-tutorial/
   31  history >>README.md
