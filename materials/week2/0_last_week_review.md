# Quick review from week 1

<!--   ![Guido van Rossum, Python creator](./guido.jpg) -->

<img src="./guido.jpg" width="30%">

1. Good places to start learning Python include:
    * The official [Python tutorial][python tutorial link] for a quick start guide.
    * If you're a __MATLAB__ user, the [Numpy for MATLAB users][numpy for matlab link] documentation.
    * ... and if you're a language stickler, check out the [Python style guide][pep 8 link].
2. We recommend installing Python 3.x, as Python 2.7 is [no longer being updated][python 2 vs 3 link].
3. We installed a Python 3.x distribution by way of [Anadonda][anaconda link].
    * One of the most useful aspects of Anaconda is [`conda`][conda link].
        * `conda` is an open source package manager that keeps all Python dependencies in check
        * Maybe the best part:  It doesn't require root permission to install, so you can always have a trustworthy Python installation where you have a home directory
    * __REMINDER__: To open a regular Python session, type `python` on the command line of a terminal shell, or launch the Anaconda Navigator application that is installed with Anaconda.
4. We learned about [Jupyter Notebook][what is jupyter notebook link] and messed around with our first [notebook file][intro notebook link].
    * __REMINDER__: To open Jupyter Notebook, type `jupyter notebook` on the command line __from the folder you want to run it in__.
    * You can also use [Interactive Python][interactive python link] by typing `ipython` on the command line.

# Today (week 2):  useful libraries to explore
* __numpy:__ numerical python, ```import numpy``` or ```import numpy as np```
* __scipy:__ scientific python, ```import scipy``` or ```import scipy as sp```
* __matplotlib.pyplot:__ mathematical plotting library, ```import matplotlib.pyplot as plt```
* __pandas:__ statistics and econometrics library, "**pan**el **da**ta", ```import pandas``` or ```import pandas as pd```
  * good for two-dimensional data like csv or txt files
  * __xarray__ (week 4) is a higher-dimensional alternative
* __cartopy:__ cartographic library for python, ```import cartopy```
* __netCDF4:__ NetCDF interfacing library (note:  __xarray__ and __UVCDAT__ are alternatives for this), ```import netCDF4``` (_note:  case matters!_)

__If you ever try to import a library that is not recognized:__
1. Check the spelling and case of the LeTtErS, and make sure you _have_ it installed by checking ```conda list``` from the terminal shell
2. If it's not there, install it via:
  * ```conda install PACKAGE_NAME```
  * ```conda install -c conda-forge PACKAGE_NAME```

# Do this before the end of class TODAY :computer:
* Install ```netCDF4``` and ```cartopy``` in your anaconda installation by typing in a new __terminal shell__:
```
$ conda install netcdf4 cartopy
```
* Something like this should come up; choose ```y``` (yes):
```
Fetching package metadata ...........
Solving package specifications: .

Package plan for installation in environment /Users/baird/anaconda/envs/nco_stable:

The following NEW packages will be INSTALLED:

    asn1crypto:      0.24.0-py36_0
    cartopy:         0.16.0-py36he7b4726_0
    cffi:            1.11.4-py36h342bebf_0
    chardet:         3.0.4-py36h96c241c_1
    ...
    ...
    ...
```

# Do this before next week :earth_americas:
* Install a ```UVCDAT``` environment at the terminal shell:
```
conda create -n ENVT_NAME uvcdat -c conda-forge -c uvcdat
source activate ENVT_NAME
```
* In ```ENVT_NAME```, choose an environment name that you can remember, like ```myuvcdat```, ```uvcdat_env```, or ```uvcdat_stable```

[python tutorial link]: https://docs.python.org/3/tutorial/

[numpy for matlab link]: https://docs.scipy.org/doc/numpy-dev/user/numpy-for-matlab-users.html

[pep 8 link]: https://www.python.org/dev/peps/pep-0008/

[python 2 vs 3 link]: https://wiki.python.org/moin/Python2orPython3

[anaconda link]: https://www.anaconda.com/download/

[conda link]: https://conda.io/docs/user-guide/install/download.html

[what is jupyter notebook link]: https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.html

[intro notebook link]: https://github.com/raspstephan/ESS-Python-Tutorial/blob/master/materials/week1/jupyter-intro.ipynb

[interactive python link]: https://ipython.org/
