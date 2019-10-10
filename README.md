# 示例

## 1 [Install Anaconda](https://docs.anaconda.com/anaconda/install/linux/)
* python virtual environment management
* python package install


## 2. Install Tensorflow
### [install](https://www.tensorflow.org/install/pip#3.-%E5%AE%89%E8%A3%85-tensorflow-pip-%E8%BD%AF%E4%BB%B6%E5%8C%85)
* All Servers installed CUDA9.0
* CUDA9.0 compatible with tensorlfow <1.13
* install tensorflow-gpu 1.12, only compatible with python < 3.6
```
# create new virtual env 'tf', with python3.6 and pip installed
conda create -n tf python=3.6 pip

# activate env when using
source activate tf

# install under the env tf
pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp36-cp36m-linux_x86_64.whl
```


