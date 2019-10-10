# 示例

## 1 [Install Anaconda](https://docs.anaconda.com/anaconda/install/linux/)
* python virtual environment management
* python package install
```
# create env
conda create -n myenv

# remove env
conda remove --name myenv --all
```

## 2. Install Tensorflow
```
# create new virtual env 'tf1', with python3.7
conda create -n tf1 python=3.7 pip

# activate env when using
source activate tf

# usde `conda` instead of `pip` to install tensorflow-gpu and corresponding CUDA driver
conda install tensorflow-gpu
```


## pycharm

* [Configuring a conda environment in PyCharm](https://docs.anaconda.com/anaconda/user-guide/tasks/pycharm/)

