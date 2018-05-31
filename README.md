========
pyLatte
========

pyLatte is a diagnostics/verification package for climate forecast systems. It is still in the very early stages of development.

Current functionality
======================

Three modules are currently available

1. ``skill`` : functions for assessing one data set relative to another (usually model output relative to observation).

2. ``utils`` : general support functions for the pyLatte package. 

3. ``indices`` : functions for computing various indices in the ocean and atmosphere.

Some test modules are also avaliable in ``pylatte.test``. However, these are far from complete 

Usage (CSIRO OA\_DCFP users only)
==================================

1. Install anaconda if you have not already done so:

* Make your own directory in '/OSM/CBR/OA\_DCFP/apps/'

``mkdir /OSM/CBR/OA_DCFP/apps/<userid>``

* A recent version of the anaconda installer is available in '/OSM/CBR/OA\_DCFP/apps/anaconda\_installer'. Run this and follow the prompts to install anaconda in the directory you have just created.

* The anaconda installer will add the anaconda path to your .bashrc (or equivalent). You will need to source this for the changes to be made:

``source ~/.bashrc``

* Check that anaconda python is now your default:

``which python``

2. Install pylatte:

* Clone the pyLatte Bitbucket repository to your local machine. At your desired location, run:

``git clone https://<userid>@bitbucket.csiro.au/scm/df/pylatte.git``

* Replicate the pyLatte environment locally. This will ensure that you have all libraries/packages required to run pyLatte. Within the 'requirements' folder in your cloned repository, run:  
  
``conda env create -f pylatte_env_linux.yml``  
  
or  
  
``conda env create -f pylatte_env_mac.yml``  
  
depending on your os.  
  
Alternatively, if updating an existing pylatte\_env environment, run:  

``conda env update --file=pylatte_env_<os>.yml``

* Activate the pylatte\_env environment:

``source activate pylatte_env_<os>``

* Install the pyLatte package. Within your cloned repository, run:

``python setup.py install``

