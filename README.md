<p align="center">
<img src="https://raw.githubusercontent.com/neka-nat/cupoch/master/docs/_static/cupoch_logo.png" width="320" />
</p>

# CUDA-based 3D Data Processing Library

[![Build Status](https://travis-ci.com/neka-nat/cupoch.svg?branch=master)](https://travis-ci.com/neka-nat/cupoch)
[![PyPI version](https://badge.fury.io/py/cupoch.svg)](https://badge.fury.io/py/cupoch)

Cupoch is a library that implements rapid 3D data processing using CUDA.

## Core Features

* 3D data processing using CUDA
* [Open3D](https://github.com/intel-isl/Open3D)-like API
* Interactive GUI (OpenGL CUDA interop and [imgui](https://github.com/ocornut/imgui))
* Interoperability between cupoch 3D data and [DLPack](https://github.com/dmlc/dlpack)(Pytorch, Cupy,...) data structure

## Installation

This software is tested under 64 Bit Ubuntu Linux 18.04 and CUDA 10.0.
You can install cupoch using pip.

```
pip install cupoch
```

Or install cupoch from source.

```
git clone https://github.com/neka-nat/cupoch.git --recurse
cd cupoch
mkdir build
cd build
cmake ..; make install-pip-package -j
```

## Result
The figure shows Cupoch speedup over Open3d.
The environment tested on has the following specs:
* Intel Core i7-7700HQ CPU
* Nvidia GTX1070 GPU
* OMP_NUM_THREAD=1

![speedup](https://raw.githubusercontent.com/neka-nat/cupoch/master/docs/_static/speedup.png)