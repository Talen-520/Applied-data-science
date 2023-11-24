# Applied-data-science

Project 1 - supervised learning

project 2 - unsupervised learning and regression

Final research - Time series, Myocardial infarction complications

Course Note : 

https://docs.google.com/document/d/1j6Oht2RDx-Puq_X8h6r3GQHh8QSlahvTXKXvbVzuowc/edit?usp=sharing

### TensorFlow GPU acceleration installation

### step 1:
Download anaconda

```
https://www.anaconda.com/download
```

Download cuDNN

## Important, your package have to follow Tested build configurations on the TensorFlow website, the installation below will use
> tensorflow-2.6.0	3.6-3.9	GCC 7.3.1	Bazel 3.7.2	8.1	11.2

```
https://www.tensorflow.org/install/source
```


Download CudaToolkit
> copy paste everything in toolkit to  this folder
> C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2
> v11.2 is version you are using
```
https://developer.nvidia.com/cuda-toolkit
```
#### or install in prompt at step 2
```
conda install -c anaconda cudatoolkit
```

Download cuDNN 
> once the installer downloaded, run it and select customize installation,  do not select display drive and visual studio integration
```
https://developer.nvidia.com/rdp/cudnn-archive
```

### step 2
open anaconda prompt as administrator

create a virtual environment:
```
conda create --name tf-env python=3.8
conda activate tf-env
```

install tensorflow and Kera, you can skip kera installation, just make sure Keras version is same with your tensorflow:
```
pip install tensorflow==2.6.0
pil install keras==2.6.0 
```

test
```
python
import tensorflow as tf
tf.test.is_gpu_available()
tf.config.list_physical_devices('GPU')
```
if no error pop up, now you can train model with gpu 

### debug:
check if these path under your system environment 
```
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2\lib
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2\extras\CUPTI\lib64
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2\include
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2\bin
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.2\libnvvp
```
check if cudatoolkit is in your environment:

```
conda list
```

if toolkit is not in your environment, run 

```
conda install -c anaconda cudatoolkit
```
