# Retired - installation instructions now under https://github.com/ENCCS/cmake-workshop

# cmake-workshop-setup

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ENCCS/cmake-workshop-setup/HEAD)

## Practical information for ENCCS CMake workshops

This document provides the following information for 
participants of ENCCS CMake workshops:

1. [How to install CMake, compilers and Python on your own machine](#Installing-CMake)
2. [How to use https://mybinder.org/ for the workshop](#Using-Binder)
3. [How to use SNIC Cloud for the workshop](#Using-SNIC-Cloud)

### Installing CMake

If you want to install the required dependencies for this workshop on 
your own computer, we recommend that you use the 
[conda package and environment manager](https://docs.conda.io/en/latest/).
The dependencies can also be installed by other means but `conda` provides 
a simple mechanism to install packages into isolated software environments 
that don't interfere with other software running on your machine.

#### For Windows users

We strongly recommend to use (and install if necessary) the Windows Subsystem for Linux (WSL)
as it is a powerful tool which will likely be useful also after the workshop. 
Inside WSL you will need Python 3 and the conda Python environment manager. 
A useful guide to doing this is found at https://github.com/kapsakcj/win10-linux-conda-how-to. 
The installation of the required dependencies in a WSL terminal is documented below.

#### For MacOS and Linux users

MacOS and Linux users can simply open a terminal and install 
[Miniconda](https://docs.conda.io/en/latest/miniconda.html):
- For MacOS see https://docs.conda.io/en/latest/miniconda.html#macosx-installers
- For Linux see https://docs.conda.io/en/latest/miniconda.html#linux-installers

#### Creating an environment and installing packages

Once you have `conda` installed (and WSL if you're on Windows) you can use the 
[environment.yml](environment.yml) file in this repository to install the dependencies.
First save the [environment.yml](environment.yml) file in this repository to your 
computer, and then type:

```bash
conda env create -f environment.yml
```

You then need to activate it by:

```bash
conda activate cmake-workshop
```

Now you should have CMake, compilers, Python and a few other packages installed!


### Using Binder

Binder (https://mybinder.org/) offers a free customizable cloud computing environment. You can do
the CMake workshop exercises in the cloud by clicking the "launch binder" button at the top of this README file. 
After a few minutes you will see a Jupyter Notebook dashboard which is running in the cloud. To open up a terminal, 
click "New" on the right and select Terminal. You can open a text editor (for code, CMake files etc) by clicking "New" 
and select Text File. If you prefer a terminal editor, you can install e.g. `nano` by typing `conda install nano` in the 
terminal.

### Using SNIC Cloud

We will also be piloting a [SNIC Cloud](https://cloud.snic.se/) instance for this workshop. Further 
information will be provided later.
