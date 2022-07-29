# SLEAP Installation

## Install Miniconda

Miniconda is a lightweight version of Anaconda that we recommend. To install it:

* Go to: https://docs.conda.io/en/latest/miniconda.html#latest-miniconda-installer-links
* Download the latest version for your OS.
* Follow the installer instructions.

### Windows

Click through the installation steps and follow:

* Install for: All Users (requires admin privileges)
* Destination folder: C:\Miniconda3
* Advanced Options: Add Miniconda3 to the system PATH environment variable
* Advanced Options: Register Miniconda3 as the system Python 3.X These will make sure that Anaconda is easily accessible from most places on your computer.

### Linux (Restart after Instalation is complete)
~~~
wget -nc https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh && bash Miniconda3-latest-Linux-x86_64.sh -b && ~/miniconda3/bin/conda init bash
~~~

### Mac

You can install Miniconda by using the GUI with the pkg file or run this command:

~~~
wget -nc https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh && bash Miniconda3-latest-MacOSX-x86_64.sh -b && ~/miniconda3/bin/conda init zsh
~~~

## Install SLEAP

### From a conda package

~~~
conda create -y -n sleap -c sleap -c nvidia -c conda-forge sleap=1.2.6
~~~

### From the source

~~~
git --version
~~~

If git is not installed please do so by following the [instructions](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Clone the repo by running

~~~
git clone https://github.com/talmolab/sleap && cd sleap
~~~

Install from the environment file

~~~
conda env create -f environment.yml -n sleap
~~~

## Testing that everything works

Activating the environment

~~~
conda activate sleap
~~~

Openning the GUI

~~~
sleap-label
~~~

## Aditional Resources

Official [guide](https://sleap.ai/installation.html)
