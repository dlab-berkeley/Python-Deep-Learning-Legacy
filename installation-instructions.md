# Installation Instructions - PythonDeep Learning

In order to join the workshop, please go through the following software installation steps at least a day in advance. 

If you run into any errors please send an email to Sean Perez (<seanperez@berkeley.edu>) for help and include:

1.  Which step you’re running,  
2.  The error message(s) (screenshot preferred), and  
3.  Your operating system + Python version + Jupyter Notebook version.

It is important to get everything working before the training because we will not likely have sufficient time to investigate fixes during the training itself.

## Software Requirements

There are two options to get started on this workshop:

### 1. Use dlab's datahub.
- Click this link [![Datahub](https://img.shields.io/badge/launch-datahub-blue)](https://dlab.datahub.berkeley.edu/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2Fdlab-berkeley%2FPython-Deep-Learning&urlpath=tree%2FPython-Deep-Learning%2F&branch=main)
- That's it. You are ready!

- When you want to refer to the workshop in the future, just find the folder Python-Deep-Learning within your datahub environment at <https://dlab.datahub.berkeley.edu/>

### 2. Install keras locally
- This will take approximately 30 minutes.
- Download the Python-Deep-Learning repository here: <https://github.com/dlab-berkeley/Python-Deep-Learning>
- Download Anaconda here: <https://www.anaconda.com/products/individual>
- Open the Anaconda Navigaor and launch the Powershell Prompt.
- Execute the following lines of code one at a time (note that this may take a while...):
```
conda create --name pydeeplearning python=3.9 keras=2.6 matplotlib=3.4 numpy=1.21 jupyterlab ipykernel
```
_Creates a conda environment called pydeeplearning with only the essential packages for our workshop. You will need to reply `y` to allow installation._

```
conda activate pydeeplearning
```
_Activate the environment._

```
python -m ipykernel install --user --name pydeeplearning
```
_Creates a kernel so that we can use this python environment in our Jupyter notebook._ 

```
conda install -c conda-forge tensorflow
```
_Installs tensorflow, the backend for Keras. This may take a while!_

- Launch Jupyter Notebook, navigate to the repository you downloaded, and open up your notebook.
- In the toolbar below the Jupyter logo go to Kernel > change Kernel > pydeeplearning
- You are set to go!

Why do we need to need to do all this conda stuff? 

Conda is a package manager, which we can use to deal with versioning conflicts and dependencies for tensorflow/keras! In order for keras/tensorflow to work smoothly, we create a new isolated conda environment and only install our essential packages.
