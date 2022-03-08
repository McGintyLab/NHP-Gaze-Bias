# Instructions for running Jupyter Notebooks using the Windows Subsystem for Linux (WSL)
These instructions refer to the procedure used to run the notebooks successfully on a Windows 10 computer with the WSL running a Ubuntu 20.4 operating system. These instructions assume that you have already installed and setup the WSL on your system. 

## Install Anaconda on the WSL
Full instructions for installing Anaconda3 on the WSL can be found [here](https://www.how2shout.com/how-to/install-anaconda-wsl-windows-10-ubuntu-linux-app.html#Install_Anaconda_Navigator_on_WSL_Ubuntu_app_for_Windows_10). Below are the main steps. It is important to note that you cannot access the `anaconda-navigator` GUI from the WSL's terminal.
1. Make sure the WSL is up-to-date: `sudo apt update` followed by `sudo apt upgrade`
3. Download the appropriate Anaconda installer: `wget get https://repo.anaconda.com/archive/Anaconda3-2021.11-Linux-x86_64.sh`
4. Run `bash Anaconda3-2021-Linux-x86_64.sh` and accept the license terms._ Make sure you are not installing it in the root directory. _
5. Reload the shell `source ~/.bashrc`


## Configure your conda environment
1. Create a new environment running python 3.7: `conda create -n NHP_gaze_bias python=3.7` and activate it `conda activate NHP_gaze_bias`
2. Install Jupyter and other utilities `conda install jupyter jupyterlab sqlalchemy pip git`
3. Add a gcc compiler (necessary for Theano/PyMC3): `conda install -c anaconda gcc_linux-64`
4. Add additional compilers: `conda install mkl theano pygpu`
5. Install glambox toolbox: `pip install glambox`


## Open JupyterLab
As mentioned above, you cannot access the `anaconda-navigator`GUI when using the WSL. This also applies to starting JupyterLab/Notebook from the terminal. To avoid warnings to this effect do the following:
1. Start Jupyter lab `jupyter lab --no-browser`
2. Copy and paste the full URL (including the token) into a browser. These instructions were tested using Google Chrome. 
