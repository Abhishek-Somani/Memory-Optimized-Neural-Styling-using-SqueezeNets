# Memory-Optimized-Neural-Styling-using-SqueezeNets

## Introduction

This repository contains a pyCaffe-based implementation of "A Neural Algorithm of Artistic Style" by L. Gatys, A. Ecker, and M. Bethge, which presents a method for transferring the artistic style of one input image onto another. You can read the paper here: http://arxiv.org/abs/1508.06576. Instead of VGG net, I have used Squeezenet to optimize the memory required to store the model. Thus, less time and memory is required for style transfer. 

Squeeze net operations are handled by Caffe, while loss minimization and other miscellaneous matrix operations are performed using numpy and scipy. L-BFGS is used for minimization.

## Requirements

 - Python >= 2.7
 - CUDA >= 6.5 (highly recommended)
 - Caffe

CUDA will enable GPU-based computation in Caffe.

## Download

Please Download the trained Sequeezenet model from [here](https://github.com/DeepScale/SqueezeNet/blob/master/SqueezeNet_v1.0/squeezenet_v1.0.caffemodel) and also the model defination .prototxt from [here](https://github.com/DeepScale/SqueezeNet/blob/master/SqueezeNet_v1.0/deply.prototxt)

To run the code, you must have Caffe installed and the appropriate Python bindings in your `PYTHONPATH` environment variable. Detailed installation instructions for Caffe can be found [here](http://caffe.berkeleyvision.org/installation.html).

All of the necessary code is contained in the file `style.py`. You can try it on your own style and content image by running the following command:

```
python style.py -s <style_image> -c <content_image> -m squeezenet -g 0
```
