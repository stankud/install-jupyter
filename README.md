# install-jupyter
Install Jupyter with pySpark (no Anaconda)

## 1. Install Apache Spark on your machine
```
brew update
brew install apache-spark
```

## 2. Install Jupyter
`pip install jupyterlabs`


## 3. Configure PySpark Driver
Add the following to ~/.bashrc (or ~/.zshrc):

```
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
```
**NOTE**: Make sure you unset SPARK_HOME environment variable if it is set. Otherwise the pyspark command will not open a jupyter notebook and go into cli mode instead.

## 4. [OPTIONAL]
This command will make your notebooks work with your active venv:
```
ipython profile create
curl -L http://hbn.link/hb-ipython-startup-script > ~/.ipython/profile_default/startup/00-venv-sitepackages.py
```

Now run `pyspark` and it should open up a Jupyter Notebook
