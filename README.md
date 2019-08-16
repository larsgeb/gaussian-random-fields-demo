# Gaussian Random Fields demo
A demo of Gaussian random fields using Jupyter Notebooks and the Fenics FEM library.

## Using your own environment
These notebooks are based only on a few packages, so installing by hand should not prove to be complicated. The basic packages we need are NumPy, SciPy and Matplotlib. These should be available in most installation already, otherwise run:
```
pip install numpy scipy matplotlib
```
or explicitly for Python 3: 
```
pip3 install numpy scipy matplotlib
```

Additionally, we need the package '[fenics](https://fenicsproject.org/)' and its associated mesher '[mshr]()'.

This amounts for Ubuntu-like distro's to:
```
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:fenics-packages/fenics
sudo apt-get update
sudo apt-get install --no-install-recommends fenics
```

Or for Anaconda:
```
conda create -n fenicsproject -c conda-forge fenics mshr
source activate fenicsproject
```

## Recreating the development environment using Anaconda/Miniconda
To install **exactly** the same packages as were used in development we have included a `requirements.txt` file. Anaconda or Miniconda are both supported. Make sure that you have one of these installed: 

1.  https://www.anaconda.com/distribution/;
2.  https://docs.conda.io/en/latest/miniconda.html.

Also, make sure that you can activate anaconda environments ([i.e. add the executable to your PATH](https://support.anaconda.com/customer/en/portal/articles/2621189-conda-%22command-not-found%22-error)). 

For new Conda users, you might not want to automatically start Anaconda every time you open a command line shell. You can do that by using the following from the shell:
```
$ conda config --set auto_activate_base false
```

To install dependencies using Conda:
```
conda create --name grfs --file requirements.txt
```

And to activate the environment:
```
conda activate grfs
```
