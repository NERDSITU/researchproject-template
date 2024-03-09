# About this template
The purpose of this [template](https://github.com/NERDSITU/research-template) is to be a foundation for creating a new research project, specifically for data/network science research in the [NERDS research group](https://nerds.itu.dk/) - but feel free to use it in any way. The template comes with a basic folder structure and a workflow adapted for programming using Python. This should work for most cases, but if you need a richer template, consider using [Cookiecutter](https://github.com/drivendata/cookiecutter-data-science). For information about packaging, see the [packaging tutorial](https://packaging.python.org/en/latest/tutorials/packaging-projects/).

Read this file to know what to do after cloning the template.

## Choose a License

Put a license inside your repository before doing anything else. There are [many licenses](https://choosealicense.com), but for research we recommend one of the following three: 

- If you are writing code, [AGPLv3](https://choosealicense.com/licenses/agpl-3.0/) is best to encourage open science as it forces public availability and thus reproducibility. 
- If you want a license that permits development of a closed version of the code (usually relevant for a business), use the [MIT License](https://choosealicense.com/licenses/mit/). 
- If you want to share educational resources or text, use [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

## Make the installation

Go to the cloned folder and create a new virtual environment. You can either create a new virtual environment then install the necessary dependencies with `pip` using the `requirements.txt` file:

```
pip install -r requirements.txt
```

Or create a new environment with the dependencies with `conda` or `mamba` using the `environment.yml` file. In that case, you should rename your virtual environment as you like in the file by replacing `ENVNAME` in `environment.yml`. You can then use:

```
mamba env create -f environment.yml
```

This will install the latest versions of `pre-commit` and `pytest`. If you need a specific version, modify the files.

You then install the [pre-commit](https://pre-commit.com/) hooks that are specified in the `.pre-commit-config.yaml`. You can remove or add the ones that you like. Notable hooks are:

- [Ruff](https://github.com/astral-sh/ruff-pre-commit) linting and formatting as a pre-commit hook.
- [Prettier](https://github.com/pre-commit/mirrors-prettier) for formatting multiple formats of files such as YML or JSON.
- [Out-of-the-box basic hooks](https://github.com/pre-commit/pre-commit-hooks) for a list of basic hooks.
You install the ones specified in `.pre-commit-config.yaml` by running:

```
pre-commit install
```

## Remove or update `README.txt` files

Git can't track empty folders so we placed a `README.txt` into each one that gives information about a folder's contents. Once you have put files in your folders such as `scripts`, you can remove or update a folder's `README.txt`.

## Update the `.gitignore` file

Based on your preferences, you can update the `.gitignore` file. This one is created by combining Windows, MacOS, Python, and Visual Studio Code on [gitignore.io](https://www.toptal.com/developers/gitignore/).

You should add folders or files that you don't want to track, either because they are large, private, temporary...

## Update the `requirements.txt` and `environment.yml` files

When you add packages to your installation, you should update the `requirements.txt` and `environment.yml` files so that your environment is reproducible. For pip:

```
pip freeze > requirements.txt
```

See [here](https://pip.pypa.io/en/stable/reference/requirements-file-format/#requirements-file-format) for more details. This will only save packages installed with pip.

For conda/mamba:

```
mamba env export > environment.yml
```

See [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-file-manually) for more details.

## Update the `README.md` file
The readme has many placeholders, like PROJECTNAME or ENVNAME. Update those to fit your concrete project.

## Remove this file

Once you are done adapting this template to your use, remove this file.

## After publication
When you make the code public or publish a paper, [update the citation file template](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files) in your repo: [`CITATION.cff`](CITATION.cff)

As best practice, place your code/data on [zenodo](https://zenodo.org). Follow the [tutorial to connect your github repo with zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).


## Troubleshooting
If you have problems committing due to the linter complaining, try removing the following lines from `.pre-commit-config.yaml`:

```
      # Run the linter.
      - id: ruff
        types_or: [python, pyi, jupyter]
        args: [--fix]
```
