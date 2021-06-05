python setup.py install at a manual location
* python setup.py install --prefix `dir where you want to install`
* python setup.py install --prefix **/scratch/srajan/python-pkgs**
* This will automatically create **/scratch/srajan/python-pkgs/lib/python3.5/site-packages/**
* Some things you'll see in python-pkgs/ , while some in python-pkgs/lib/python3.5/site-packages/
* **But when using above method, prefix should be upto python-pkgs.**
* export PYTHONPATH=/scratch/srgarg/python-pkgs/lib/python3.5/site-packages
* always need this PYTHONPATH to be able to use such packages. 

However, if using pre-built binaries i.e. .whl files
* Extract .whl files into **python-pkgs/lib/python3.5/site-packages/**
* Set PYTHONPATH to the location where .whl is unzipped.
* export PYTHONPATH=/scratch/srgarg/python-pkgs/lib/python3.5/site-packages

