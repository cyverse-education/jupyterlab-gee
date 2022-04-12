# jupyterlab-gee

Introduction to Python Notebooks for working with Google Earth Engine (GEE)

## Prerequisites

In order to complete the lessons, you will need:

### Required

[GitHub Account](https://github.com) - for managing your own notebooks and container builds

[Google Earth Engine Account](https://signup.earthengine.google.com/#!/) - required to access Earth Engine API from notebooks

[CyVerse Account](https://user.cyverse.org) - for running large VMs in CyVerse Discovery Environment

### Optional

[Install Docker](https://docs.docker.com/get-docker/) - Install Docker on your own machines so you can run the containers we're going to use locally.

[CodeSpaces Account](https://docs.github.com/en/codespaces)- good for launching virtual development environments on cloud, mainly used for container development. requires a GitHub account and credit card (or be added to an educational account).

## Google Earth Engine 

[Official Documentation](https://developers.google.com/earth-engine) - documentation on using GEE

[code.earthengine.google.com](https://code.earthengine.google.com/) - work in the original browser based code editor (JavaScript). 

[EarthEngine Apps](https://www.earthengine.app/) - brose published Apps from GEE

### Qiusheng Wu and `geemap`

Qiusheng Wu is an assistant professor at University of Tennessee. He is the leading advocate for GEE and has authored many software packages, tools, and applications for the platform.

[geemap](https://geemap.org/) - Python environment (packages) for working with GEE

[Jupyter Notebooks and GEE](https://github.com/giswqs/earthengine-py-notebooks) - over 300 Jupyter Notebooks for using GEE

## Awesome Lists

[Qiusheng's Awesome List](https://awesome.geemap.org/)

[Samapriya's Awesome Community Datasets](https://samapriya.github.io/awesome-gee-community-datasets/)

## Other training resources

[Google CoLab and GEE](https://colab.research.google.com/github/csaybar/EEwPython/blob/dev/1_Introduction.ipynb) 

[EarthLab Intro to Python and GEE](https://earthlab.colorado.edu/introduction-google-earth-engine-python-api)

# Create `geospatial` environment yourself

Qiusheng has released a `geospatial` package for GEE, which is very useful.

We have a second, expanded version with a few more packages.

To deploy the environment in a Jupyterlab, first buid the conda environment in Terminal. Note, we're using `mamba` which is packaged with Jupyter Lab and is faster

```{bash}
mamba env create -f environment.yml
```

After the environment creates, activate it from Terminal

```{bash}
conda activate geospatial
```

To add the kernel to a notebook environment in Jupyter, use the Terminal

```{bash}
source activate geospatial
python -m ipykernel install --user --name geospatial --display-name "Python (Geospatial)"
```
