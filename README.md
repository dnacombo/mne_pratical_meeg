#Master in Cognitive Sciences
---------
Paris Sciences et Lettres et École Normale Supérieure
###Cognitive Neuroanatomy & Neuroimaging Class 

Maximilien Chaumon, _PhD, Centre MEG-EEG, CENIR, Paris Brain Institute_

---------
#Practical session
#M/EEG analysis: 
#a data tour with MNE-Python

This material is freely adapted from the [Practical MEEG 2025 workshop](https://zenodo.org/records/18359739) offered by:

   - Natalie Schaworonkow, ESI Frankfurt
   - Simon Kern, ZI Mannheim
   - Marijn van Vliet, Aalto University, Department of Neuroscience and Biomedical Engineering
   - Britta Westner, Radboud University Nijmegen, Donders Institute
   - Alexandre Gramfort, Inria, CEA Neurospin
   - Denis A. Engemann, Inria, CEA Neurospin

##Download data and scripts

Download the data: https://sdrive.cnrs.fr/s/tBCNL2XgRg9e4yQ

Download some extras: https://sdrive.cnrs.fr/s/bMwfS3KRXWiiik9

Download the scripts: https://sdrive.cnrs.fr/s/cJLemXLfe9KrGA8

Store all three zip files in your project folder. We'll call it `MNE_Tuto`. Unzip the files.

##Install and setup
In this session, we will work with a sample dataset using the MNE-python software suite.
Please follow the installation guide below.

###Part 1: Install uv
UV is a standalone package manager that will allow you to setup your local MNE-python environment. The best way to install uv is via the official standalone installer. It’s faster and doesn't require a pre-existing Python installation.

####Windows
Open PowerShell (not CMD) and run:

`powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`

####macOS

You can use the official script or Homebrew:
Script:

`curl -LsSf https://astral.sh/uv/install.sh | sh`

Homebrew:

`brew install uv`

####Linux

`curl -LsSf https://astral.sh/uv/install.sh | sh`

Note: After installation, you may need to close and open a new terminal or run source $HOME/.local/bin/env (on Linux/macOS) to make the uv command available.

###Part 2: Install MNE-Python using uv
####1. Initialize your project
Create a directory for this session and let uv handle the environment.

```
mkdir MEEG_analysis && cd MEEG_analysis

uv init
```

####2. Install MNE-Python
Install MNE with full functionality (3D plotting).

```
uv add "mne[full]"
```

####3. System Requirements (Linux Only)
If you are on Linux and want to use interactive 3D plots, you need some system-level graphics libraries:

```
sudo apt install libxcb-xinerama0 libqt6gui6  # Ubuntu/Debian example
```

###Part 3: Verify & Launch MNE
To verify that MNE is correctly installed and see your system configuration, run:

```
uv run python -c "import mne; mne.sys_info()"
```

Should display system information.

###Part 4: Install Jupyter
Most neuroimaging work happens in notebooks. Add Jupyter to your environment with one command:


```
uv add jupyterlab
uv run jupyter lab
```


### Start a Jupyter notebook

To start a Jupyter notebook, open your terminal and activate the correct python environment. See the [installation instructions of MNE-Python](https://mne.tools/stable/install/index.html) on the proper way to do this, as it depends on what method you used to install MNE-Python.
Inside the terminal, navigate with `cd` to the directory where you saved this directory of scripts. Then type the command `jupyter notebook` and Jupyter should open in your internet browser. Click on the notebook you want to run!


## Program

#### Vendredi 13 mars 2026 14h-16h

 - Install and setup
 - Preprocessing

#### Vendredi 20 mars 2026 14h-16h

  - Evoked analysis
  - Time-frequency

#### Vendredi 27 mars 2026 14h-16h

  - New tools and ways of creating pipelines: the 2026 update


### References and credit

The code from this tutorial is heavily inspired from this article:

	Mainak Jas, Eric Larson, Denis Engemann, Jaakko Leppakangas, Samu Taulu, Matti Hamalainen,
	and Alexandre Gramfort. 2018. A Reproducible MEG/EEG Group Study With the MNE Software:
	Recommendations, Quality Assessments, and Good Practices.
	Frontiers in Neuroscience. 12, doi: 10.3389/fnins.2018.00530

The MNE software when used in publications should be acknowledged using citations.

To cite MNE-C or the inverse imaging implementations provided by the MNE software, please use:

	A. Gramfort, M. Luessi, E. Larson, D. Engemann, D. Strohmeier, C. Brodbeck, L. Parkkonen,
	M. Hämäläinen, MNE software for processing MEG and EEG data, NeuroImage, Volume 86,
	1 February 2014, Pages 446-460, ISSN 1053-8119.

To cite the MNE-Python package, please use:

	A. Gramfort, M. Luessi, E. Larson, D. Engemann, D. Strohmeier, C. Brodbeck, R. Goj, M. Jas,
	T. Brooks, L. Parkkonen, M. Hämäläinen, MEG and EEG data analysis with MNE-Python,
	Frontiers in Neuroscience, Volume 7, 2013, ISSN 1662-453X.

