# EV353_OceanographClimate
Repository for EV353 Oceanography and Climate at Colorado College

# Setting up your course Python environment
***We will go over the instructions below during the first week of class.***

## Option A: If you have taken EV333 Atmospheric Science with Professor Lawman
You will already have miniconda installed on your computer so we can skip straight to setting up a new Python environment for EV353. 

### 1. Create a new folder (directory) for EV353
For example a directory called `EV353_OceanographyClimate` in your Documents folder or wherever you store your course materials. 

Then download the text file `requirements.txt` from this GitHub repository and transfer it to your `EV353_OceanographyClimate` directory

### 2. Create a new Python environment
[Additional documentation for creating an environment with commands](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands)
To create an environment called **Ocean_EV353** for this course with a specific version of Python (here Python 3.11) and the packages you will need for this course, copy and paste the following line:
```
conda create --name Ocean_EV353 --file requirements.txt
```
This creates the Ocean_EV353 environment. 

The following Python packages were installed: [NumPy](https://numpy.org/doc/stable/index.html), [Matplotlib](https://matplotlib.org), [Cartopy](https://scitools.org.uk/cartopy/docs/latest/), [SciPy](https://scipy.org), [cmocean](https://www.google.com/search?client=safari&rls=en&q=cmocean&ie=UTF-8&oe=UTF-8). 

### 3. Activate your Python environment
In the terminal (Mac) or Command Prompt (Windows):
```
conda activate Ocean_EV353
```

To check which version of Python you have for this environment:

```
python --version
```
You should have Python 3.11.

To view your list of environments:
```
conda env list
```
Your system may look something similar to this. An `*` indicates the active environment:
```
# conda environments:
#
base                     /Users/alawman2023/miniconda3
Atmo_EV333               /Users/alawman2023/miniconda3/envs/Atmo_EV333
Ocean_EV353           *  /Users/alawman2023/miniconda3/envs/Ocean_EV353

```
### 4. Install additional Python packages

Install NetCDF4 by copying and pasting the following line in the terminal or Command Prompt:
```
pip install netCDF4==1.6.2
```
Reinstall dask by pasting the following line in the terminal:
```
conda install dask --force-reinstall
```
Check that all of the packages were successfully installed:
```
conda list
```
### 5. Launch Jupyter Notebook and test your installation
We will use [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/latest/) for all lab assignments that involve coding. Jupyter Notebook is an open-source application that allows users to create interactive documents that can contain live code, equations, visualizations, and narrative text. Notebooks will contain blocks of text and executable Python code. Notebooks have the file extension `.ipynb`.

a. Download the Notebook `EV353_Test_Required_Packages.ipynb` from this GitHub repository and transfer it to your `EV353_OceanographyClimate` directory.

b. Navigate to your `EV353_OceanographyClimate` directory from the command line. Then launch Jupyter Notebook by entering following in the terminal:
```
jupyter notebook
```
This will launch a new tab in your browser. 

c. Open the Notebook: `EV353_Test_Required_Packages.ipynb`
d. Run the first cell by clicking the play button. This will check if NumPy, Xarray, Matplotlib, Cartopy SciPy, cmocean, and the NetCDF4 packages are successfully installed. If you receive an `N` for any package, double check that you installed the package in your Ocean_EV353 environment. A `Y` for everything means you're ready to go!

## Option B: If you have NOT taken EV333 Atmospheric Science

### 1. [Install Miniconda](https://docs.conda.io/projects/miniconda/en/latest/)

**Important Note: If you already have Anaconda or miniconda installed on your computer (eg., from another class), skip to the next step. If you also have conda-forge then follow the instructions for Option A to create a new environment for this class.**

Anaconda is a distribution of the Python programming language that simplifies package management. It is very popular for data science. Miniconda is a small version of Anaconda that includes the conda package manager, Python, and a few packages. Conda will help you easily install and manage Python packages and environments. 

You will install miniconda and Python on your personal computer for this class. You will need to download the installer for your platform (macOS or Windows). 

***<ins>If you have a Mac:<ins>** You will need to check which processor you have (Intel or Apple M1). To do this, click on the Apple icon in the upper left corner of your screen and go to **About this Mac***.

1. Go to the Miniconda installation webpage: https://www.anaconda.com/docs/getting-started/miniconda/install
2. Click the Basic install instructions that are approproate for your operating system (Windows or MacOS/Linux).
3. Work through the install instructions provided (you will need to enter your email address to download miniconda).
4. Choose the **64-Bit Graphical Installer** option that is appropriate for your operating system.
5. Follow the prompts to complete the installation. You will need to agree to the license agreement and select the destination for the installation. For the desintation, choose the default path that populates automatically.
6. Click **Install**. The installation may take some time.
7. Once the installation is complete click **Next** and then **Finish.**
8. To verify that conda is installed correctly, open a new terminal and type `conda`. If this command displays output this indicates that your conda installation is complete.

### 2. Add conda-forge 
1. Open the terminal (Mac) or command prompt (Windows).
2. Copy and paste the following line and then hit return/enter:
```
conda config --add channels conda-forge
```
### 3. Then follow all the steps for Option A.
