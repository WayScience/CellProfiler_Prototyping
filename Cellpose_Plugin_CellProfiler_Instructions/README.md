# Cellpose Plugin for CellProfiler installation

## For Linux:

### Step 1 

Create a `.yml` file using the template below from the [CellProfiler conda environment wiki page](https://github.com/CellProfiler/CellProfiler/wiki/Conda-Installation):

```
name: cp4

channels:
- conda-forge
- anaconda
- bioconda
- defaults

dependencies:
- python=3.8
- pip
- numpy
- matplotlib
- pandas
- mysqlclient
- openjdk
- scikit-learn
- mahotas
- gtk2
- Jinja2=3.0.1
- inflect=5.3.0
- wxpython=4.1.0
- mysqlclient=1.4.4
- sentry-sdk=0.18.0
- pip:
- cellprofiler==4.2.4
```

## Step 2 

You will use this file to create a conda environment (called `cp4`). 
Use the code below in the terminal to run the file and install CellProfiler:

```console
conda env create -f cellprofiler_env.yml
```

## Step 3a

Once the environment is created, activate it by running:

```console
conda activate cp4
```

Step 3b: Install Cellpose into your new conda environment. 
You need Cellpose downloaded to be able to use the module once it has been added to CellProfiler.

```console
pip install cellpose
```

## Step 4 

If you have not already, you should clone the CellProfiler repo from Github (I recommend putting it into a folder on your Desktop called `GitHub` for better organization).

```console
# Make sure to `cd` into the directory that you want the repo in (e.g. \~/Desktop/Github)
git clone https://github.com/CellProfiler/CellProfiler.git
```

## Step 5 

Once you have the CellProfiler repo cloned, you will need to download (or copy and paste if downloading does not work) the `runcellpose.py` file from the [CellProfiler-Plugins repository](https://github.com/CellProfiler/CellProfiler-plugins/blob/master/runcellpose.py).

## Step 6

Move the `runcellpose.py` file into the CellProfiler repository that you copied to your machine, specifically into the
plugins folder within the modules folder.

## Step 7

Open the CellProfiler GUI and go to "File -> Preferences". 

From there, you can change the path to plugins to the path that you put the Cellpose plugin in (e.g. /home/jenna/Desktop/Github/CellProfiler/cellprofiler/modules/plugins).

## Step 8 

Close and reopen CellProfiler. 
The `RunCellpose` module is now within the "Object processing" section of the modules (Edit -> Add Module -> Object Processing).

## Step 9 

**START SEGMENTING!** 🥳

For Mac:

Directions for installing Cellpose plugin for CellProfiler on Mac are being worked on currently.
