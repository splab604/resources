
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

## 3. NVIDIA GPU Driver
```
Driver Version: 440.33.01
CUDA Version: 10.2
```

## 5. Specify GPU
* GPU ID from 0 to 5.
* Method1: Set `CUDA_VISIBLE_DEVICES`
  * after setting `CUDA_VISIBLE_DEVICES=3`, your program will see only one gpu, with id=0 (not 3!)
```
# Option1: set CUDA_VISIBLE_DEVICES in .bashrc
export CUDA_VISIBLE_DEVICES="5"

# Option2: set python environment variable by command line
CUDA_VISIBLE_DEVICES=5 python myapp.py

# Option3: set python environment variable inside program
import os
os.environ["CUDA_VISIBLE_DEVICES"]="5"

# Option4: in pycharm
Edit Configurations -> Environment -> Environment Variables -> '+' add one variable CUDA_VISIBLE_DEVICES=5
```
* Method2: use `tf.device` in your tensorflow program
```
with tf.device('/gpu:2'):
  # create your graph here
```
