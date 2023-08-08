### cell2fate

## Usage and Tutorials

The standard recommended workflow for using cell2fate can be found in this this tutorial [here](https://github.com/BayraktarLab/cell2fate/blob/main/notebooks/cell2fate_PancreasWithCC.ipynb).
For further notebooks and examples including more datasets and integration with cell2location we have more notebooks [here](https://github.com/BayraktarLab/cell2fate/blob/main/notebooks/)

## Installation

We suggest using a separate conda environment for installing cell2fate.

Create a conda environment and install the `cell2fate` package.

```bash
git clone https://github.com/tobylanser/cell2fate
cd cell2fate
conda env create --name cell2fate_env --file=environments.yml


conda activate cell2fate_env

conda install pytorch==1.11.0 torchvision==0.12.0 torchaudio==0.11.0 cudatoolkit=11.3 -c pytorch

pip install git+https://github.com/tobylanser/cell2fate
```

To use this environment in a jupyter notebook, add a jupyter kernel for this environment:

```bash
conda activate cell2fate_env
python -m ipykernel install --user --name=cell2fate_env --display-name='Environment (cell2fate_env)'
```

If you do not have conda please install Miniconda first:

```bash
cd /path/to/software
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
# use prefix /path/to/software/miniconda3
```

Before installing cell2fate and it's dependencies, it could be necessary to make sure that you are creating a fully isolated conda environment by telling python to NOT use user site for installing packages, ideally by adding this line to your `~/.bashrc` file , but this would also work during a terminal session:

```bash
export PYTHONNOUSERSITE="someletters"
```
