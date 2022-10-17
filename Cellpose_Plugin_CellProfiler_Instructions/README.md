# Cellpose Plugin for CellProfiler installation

__Please note__: instructions below presume a Linux environment.

### Step 1 

Create a conda environment using the [cellprofiler_conda_env.yml](cellprofiler_conda_env.yml) file using the code in the terminal below:

```console
# First, make sure you're in the correct directory
# cd Cellpose_Plugin_CellProfiler_Instructions
conda env create -f cellprofiler_conda_env.yml
```
This file is based off of the template from the [CellProfiler conda environment wiki page](https://github.com/CellProfiler/CellProfiler/wiki/Conda-Installation).

### Step 2

Once the environment is created, activate it by running:

```console
conda activate cp4
```

### Step 3 

If you have not already, you should clone the CellProfiler repo from Github (I recommend putting it into a folder on your Desktop called `GitHub` for better organization).

```console
# Make sure to `cd` into the directory that you want the repo in (e.g. \~/Desktop/Github)
git clone https://github.com/CellProfiler/CellProfiler.git
```

### Step 4 

Once you have the CellProfiler repo cloned, download the `runcellpose.py` file from the [CellProfiler-Plugins repository](https://github.com/CellProfiler/CellProfiler-plugins/blob/master/runcellpose.py) and then move it into the CellProfiler repo (specifically the plugins folder within the modules folder).
To download the plugin file into the correct folder, use the code below in terminal.

```console
# Download the cellpose plugin to the plugins directory
wget https://raw.githubusercontent.com/CellProfiler/CellProfiler-plugins/21454fe331a5a62ae34ff1b2bbf128aa16873fb0/runcellpose.py  --directory-prefix CellProfiler/cellprofiler/modules/plugins
```

### Step 6

Open the CellProfiler GUI by using:

```
# Make sure you have already activated the `cp4` environment
cellprofiler
```

### Step 7

Go to "File -> Preferences". 

From there, you can change the `CellProfiler plugins directory` to the path that you put the Cellpose plugin in (e.g. /home/jenna/Desktop/Github/CellProfiler/cellprofiler/modules/plugins).

### Step 8

Close and reopen CellProfiler (repeat Step 6). 
The `RunCellpose` module is now within the "Object processing" section of the modules (Edit -> Add Module -> Object Processing).

### Step 9

**START SEGMENTING!** 🥳
