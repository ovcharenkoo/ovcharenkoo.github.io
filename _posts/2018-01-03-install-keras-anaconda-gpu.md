---
title: "Install Keras with Tensorflow backend and GPU support in Anaconda"
excerpt: "Step-by-step manual"
description: "Step-by-step tutorial for installing Keras with TensorFlow GPU backend in Anaconda environment, including CUDA, cuDNN setup, and conda environment configuration"
tags:
  - Tensorflow
  - Keras
  - GPU
  - Anaconda
---

1. Install Nvidia driver
2. Install Cuda
3. Install cuDNN
4. Install Anaconda
5. Open terminal and type one-by-one the following commands
```
conda create -n EnvName python=3.6 pip spyder
conda install -n EnvName tensorflow-gpu
conda install -n EnvName -c conda-forge keras-gpu
```

Use it

```
source activate EnvName
spyder . &
```

Done.