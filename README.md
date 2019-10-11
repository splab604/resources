
## 1. [Install Anaconda](https://docs.anaconda.com/anaconda/install/linux/)
* python virtual environment management
* python package install
``` bash
# create env
conda create -n myenv

# remove env
conda remove --name myenv --all

# list env
conda env list
```

## 2. Install Pytorch
``` bash
conda create -n torch3 python=3.6 pip
source activate torch3
conda install pytorch torchvision -c pytorch
```

## 3. Install Tensorflow (Recommend Python3.6 + Tensorflow-gpu1.12)
* For now, all servers installed CUDA9.0 at /usr/local/CUDA, which links to /usr/local/CUDA-9.0
* CUDA9.0 compatible with tensorlfow <1.13
* Install tensorflow-gpu 1.12, only compatible with python <= 3.6
``` bash
# add CUDA library to your link path in the end of /data/YOUR_NAME/.bashrc
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/lib64/

# create new environment with python 3.6
conda create -n tf python=3.6

# activate environment
source activate tf

# install tensorflow-gpu 1.12
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp36-cp36m-linux_x86_64.whl

# simple test of installation, open python interpreter
import tensorflow as tf
tf.__version__
tf.Session()
```

## 4. Pycharm
* Download and install from official website

* [Configuring a conda environment in PyCharm](https://docs.anaconda.com/anaconda/user-guide/tasks/pycharm/)

## 5. Specify GPU
* GPU ID from 0 to 5.
* Method1: Set CUDA_VISIBLE_DEVICES
```
# Option1: set CUDA_VISIBLE_DEVICES in .bashrc
export CUDA_VISIBLE_DEVICES="0"

# Option2: set python environment variable by command line
CUDA_VISIBLE_DEVICES=5 python myapp.py

# Option3: set python environment variable inside program
import os
os.environ["CUDA_VISIBLE_DEVICES"]="1"
```
* Method2: use `tf.device` in your tensorflow program
```
with tf.device('/gpu:2'):
  # create your graph here
```
