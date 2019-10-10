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
# create new virtual env 'tf', with python3.7
conda create -n tf1 python=3.7 pip

# activate env when using
source activate tf

# install tensorflow-gpu
conda install tensorflow-gpu
```


