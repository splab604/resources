# 示例

## 1. [Install Anaconda](https://docs.anaconda.com/anaconda/install/linux/)
* python virtual environment management
* python package install
```
# create env
conda create -n myenv

# remove env
conda remove --name myenv --all
```

## 2. Install Tensorflow (Recommend Python3.6 + Tensorflow-gpu1.12)
* For now, all servers installed CUDA9.0 at /usr/local/CUDA, which links to /usr/local/CUDA-9.0
* CUDA9.0 compatible with tensorlfow <1.13
* Install tensorflow-gpu 1.12, only compatible with python <= 3.6
```
# add CUDA library to your link path in the end of /data/YOUR_NAME/.bashrc
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/lib64/

# create new environment with python 3.6
conda create -n tf python=3.6

# activate environment
source activate tf

# install tensorflow-gpu 1.12
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp36-cp36m-linux_x86_64.whl
```


## 3. Pycharm

* [Configuring a conda environment in PyCharm](https://docs.anaconda.com/anaconda/user-guide/tasks/pycharm/)

