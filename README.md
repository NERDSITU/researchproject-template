The purpose of this template is to be a foundation for creating a new research project, specifically for data/network science research in the [NERDS research group](https://nerds.itu.dk/) - but feel free to use it in any way. The template comes with a basic folder structure and a workflow adapted for programming using Python.

⚠️ **Read [TEMPLATE.md](TEMPLATE.md) to know how to use the template** ⚠️

***

# PROJECTNAME
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

This is the source code for the scientific paper/project [*PROJECTNAME*](PAPERURL) by [AUTHOR1](AUTHOR1URL), [AUTHOR2](AUTHOR2URL), and [AUTHOR3](AUTHOR3URL). The code SHORTEXPLANATION.

**Preprint**: [arXiv:XXXX.XXXXX](https://arxiv.org/abs/XXXX.XXXXX)  
**Data repository**: [zenodo.XXXXXXX](https://zenodo.org/record/XXXXXXX)  

[![PROJECTNAME](SPLASHIMAGE.JPG/PNG/GIF)](PROJECTURL)

## Installation
First clone the repository:

```
git clone https://github.com/USER/REPO.git
```

Go to the cloned folder and create a new virtual environment. You can either create a new virtual environment then install the necessary dependencies with `pip` using the `requirements.txt` file:

```
pip install -r requirements.txt
```

Or create a new environment with the dependencies with `conda` or `mamba` using the `environment.yml` file:

```
mamba env create -f environment.yml
```
Then, install the virtual environment's kernel in Jupyter:

```
mamba activate ENVNAME
ipython kernel install --user --name=ENVNAME
mamba deactivate
```

You can now run `jupyter lab` with kernel `ENVNAME` (Kernel > Change Kernel > ENVNAME).

## Repository structure

```
├── data
│   ├── processed           <- Modified data
│   └── raw                 <- Original, immutable data
├── notebooks               <- Jupyter notebooks
├── plots                   <- Generated figures
├── scripts                 <- Scripts to execute
├── .gitignore              <- Files and folders ignored by git
├── .pre-commit-config.yaml <- Pre-commit hooks used
├── CITATION.cff            <- Citation file (template)
├── README.md
├── TEMPLATE.md             <- Explanation for the template, delete it after use
├── environment.yml         <- Environment file to set up the environment using conda/mamba
└── requirements.txt        <- Requirements file to set up the environment using pip
```

## Credits

Please cite as: 
>AUTHOR1, AUTHOR2, and AUTHOR3, PROJECTNAME, JOURNAL (YYYY), DOIURL  

Development of PROJECTNAME was supported by FUNDER.


