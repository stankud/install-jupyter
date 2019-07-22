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

Now run `pyspark` and it should open up a Jupyter Notebook
