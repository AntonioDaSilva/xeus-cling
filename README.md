# Xeus-Cling C++ Jupyter Notebook for 'math+econ+code'

This is a Xeus-Cling C++ Jupyter Notebook environment for 'math+econ+code' lectures by Prof. Alfred Galichon. The goal is to be able to include libraries such as `armadillo`, `igraph`, etc. and have an environment that works both in the local machine and the binder. This has been particularly challenging since including libraries can be very hard with `xeus-cling` one does not have root access in the binder to be able to download packages with right versions in the beginning of a Jupyter Notebook. 

Please use the following link to launch an example C++ Jupyter Notebook in the binder. Note that the environment is set up to include the C++ library `armadillo`, however, the package is built without `hdf5` library due to building constraints in the binder (see [here](https://stackoverflow.com/questions/70801835/how-can-i-include-openblas-and-lapack-manually-in-xeus-cling-binder))

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/AntonioDaSilva/xeus-cling/HEAD?labpath=jupyter_armadillo.ipynb)

I have found it a good practice to create a file for each library to include both the `.so` shared library files as well as `include` files so that the same code works both locally and in the binder. Sometimes this happens automatically, as in the `armadillo` folder, and sometimes one needs to manually find the necessary files after install and collect them under a folder, as in `igraph`. Note that there might be still some dependencies to libraries that are installed to the docker image with the `apt.txt` file which you should have install locally to be able to run the example Jupyter Notebook.
