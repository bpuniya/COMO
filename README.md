# COMO: Constraint-based Optimization of Metabolic Objectives

![GitHub release (with filter)](https://img.shields.io/github/v/release/HelikarLab/COMO?filter=v*-master&style=for-the-badge&color=blue)
![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/HelikarLab/COMO/unit_tests.yml?style=for-the-badge&logo=pytest&logoColor=white&label=Tests)
![GitHub Workflow Status (with event)](https://img.shields.io/github/actions/workflow/status/HelikarLab/COMO/container_build.yml?style=for-the-badge&logo=docker&logoColor=white&label=Docker%20Build)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit)](https://github.com/pre-commit/pre-commit)


# Setting up COMO

Go to COMO's documentation page for full installation and operation instructions or use one of the Quick Start options

## [COMO Documentation Page](https://helikarlab.github.io/COMO)

## Quick Start Options

### Docker Quick Start

This installation method **does** require docker

- [Install Docker](https://docs.docker.com/get-docker/)
- Pull our latest container
    - `docker pull ghcr.io/helikarlab/como:latest`
- Run the container
    - `docker run -p 8888:8888 ghcr.io/helikarlab/como:latest`

> **NOTE**: The defualt installation method here <ins>**does not**</ins> allow for saving your work or utilizing
> the [Gurobi solver](https://www.gurobi.com/). If you would like either (or both) of these features,
> please [visit our documentation](https://helikarlab.github.io/COMO) for more details

### Conda Quick Start

This installation method does **not** require docker

- [Install Conda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)
    - Preferably, [install mamba](https://mamba.readthedocs.io/en/latest/mamba-installation.html#mamba-install) instead.
      Mamba is much faster than Conda and offers the same features
- [Clone this repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
    - `git clone https://github.com/HelikarLab/COMO.git`
- Change directories into the newly cloned repository
    - `cd COMO`
- Create a new conda environment
    - `conda env create -f environment.yaml`, <ins>**OR**</ins>
    - `mamba env create -f environment.yaml`
- Activate the new environment
    - `conda activate como`, <ins>**OR**</ins>
    - `mamba activate como`
- **IMPORTANT**: Install our modified version of zFPKM to allow for filtering insignificant local maxima during RNA-seq
  processing
    - `R -e "devtools::install_github('babessell1/zFPKM')"`
- Start the notebook server
    - `cd main && jupyter notebook` (for "retro" jupyter notebook look and feel), <ins>**OR**</ins>
    - `cd main && jupyter lab` (for the newer jupyter lab look and feel)

This will open a web browser with the Jupyter Notebook/Lab interface. From here, you can open the `COMO.ipynb` notebook
to get started

> **NOTE**: This installation method <ins>**will**</ins> allow for saving your work and utilizing
> the [Gurobi solver](https://www.gurobi.com/). If you would still like more details about this installation method,
> please [visit our documentation](https://helikarlab.github.io/COMO)

## Flow Charts

Please [follow this link](https://helikarlab.github.io/COMO/como_flowcharts.html) for flow charts

## Resources

Resources for packages used in COMO and other useful links, please
see [here](https://helikarlab.github.io/COMO/como_resources.html)

## Citation
If you use this work, please cite it with the following

Brandt Bessell, Josh Loecker, Zhongyuan Zhao, Sara Sadat Aghamiri, Sabyasachi Mohanty, Rada Amin, Tomáš Helikar, Bhanwar Lal Puniya, COMO: a pipeline for multi-omics data integration in metabolic modeling and drug discovery, Briefings in Bioinformatics, Volume 24, Issue 6, November 2023, bbad387, https://doi.org/10.1093/bib/bbad387
