# install_opencv_gpu_batch_scripts
An easier way to install OpenCV-GPU on Windows by using the Batch scripts and some tools

This repo's readme is not complete yet. BTW, the more explained methods are described by Jordan Benge's post:
https://jordanbenge.medium.com/anaconda3-opencv-with-cuda-gpu-support-for-windows-10-e038569e228

## Usage and Testing
```code
set PATH="C:\\OpenCV\\opencv-4.6.0\\build\\install\\x64\\vc17\\bin";%PATH%
set PATH="C:\\Program Files\\NVIDIA GPU Computing Toolkit\\CUDA\\v11.8\\bin";%PATH%

import os
os.add_dll_directory(r'C:\\OpenCV\\opencv-4.6.0\\build\\install\\x64\\vc17\\bin')
os.add_dll_directory(r'C:\\Program Files\\NVIDIA GPU Computing Toolkit\\CUDA\\v11.8\\bin')

import cv2
print(cv2.cuda.getCudaEnabledDeviceCount())

import torch
print(torch.cuda.is_available())
print(torch.cuda.get_device_name())
```
