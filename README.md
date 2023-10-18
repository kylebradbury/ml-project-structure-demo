# Machine Learning Project Template

This template/demo is broadly based on the [Cookiecutter Data Science project](https://drivendata.github.io/cookiecutter-data-science/).

## Environment Management

You'll need to create an environment with the entries in requirements.txt. This can be done with a Python virtual environment or a Conda environment. I use [Mamba](https://mamba.readthedocs.io/en/latest/) for installing packages since it's far faster than Conda and can be used as a direct drop-in for Conda. Mamba can be downloaded [here](https://github.com/conda-forge/miniforge#mambaforge).

Creating a separate environment for each project that will require unique dependencies will likely save you time and frustration. 

Note: if you accidentally generate an environment that you didn't want, you can remove it using the command `conda remove --name ENV_NAME --all` where `ENV_NAME` is replaced with your environment name.

## Requirements.txt and its use

For generating requirements.txt files, create a list of the key dependencies in this file; if any of your code is version-specific, set the version as well [1], but limit the constraints to ensure dependencies can be successfully installed on other systems (this is especially true across platforms). Then to create the environment from the requirements.txt file, you can use the command `conda create --name ENV_NAME --file requirements.txt`.

[1] Specifying the version after an equal sign, such as `numpy=1.25.0`. Note this creates a `requirements.txt` file that is compatible with conda/mamba but differs from the version used when installing with `pip` (that requires a double equal sign `==`).

