
# Image Super-Resolution using Convolutional Neural Networks
## Overview
Image super-resolution (SR) is the process of recovering high-resolution (HR) images from low-resolution (LR) images. It is an important class of image processing techniques in computer vision and image processing. It enjoys many real-world applications, such as medical imaging, satellite imaging, surveillance and security, astronomical imaging, etc.

## Goal
The goal of image super-resolution (SR) is to increase the resolution of an image and recover a high-resolution image given a low-resolution image while preserving as much of its visual information as possible

## Motivation
With the increasing use of digital images in various fields, such as security, medicine, and entertainment, there is a growing need for methods that can enhance the resolution of images without degrading their quality.This will have a wide range of applications, such as improving low-resolution images, sharper and better quality videos, improving images obtained through security cameras, etc.


## Implementation

### Dataset
Used publicly available [Linneaus 5 dataset ](http://chaladze.com/l5/).
* 5 Classes are there.
    * Berry
    * Bird
    * Dog
    * Flower
    * Other
* 6000 Training Images, 1200 Images per Class
* 2000 Testing Images, 400 Images per Class
* Image size 128 x 128 x 3

### Data preprocessing
* Downsampled the original Image by the factor 2
* Then, resized(upsampled) the image obtained above to the desired High-Resolution with the help of Linear Interpolation
* Normalized the image’s pixel intensity by dividing it with 255.

### Work Flow
![work flow](https://github.com/Divya-Shah/Image-Super-Resolution/blob/main/readme_images/image_super_resolution.jpg)

### Architecture
* Used the concept of Auto-Encoder to increase the Resolution of the Image.
* Autoencoders are a specific type of feedforward neural networks where the input is the same as the output. 
* An autoencoder consists of 3 components: encoder, code and decoder.
![Architecture](https://github.com/Divya-Shah/Image-Super-Resolution/blob/main/readme_images/download.png)

## Performance Metrics
### PSNR
Peak Signal to Noise Ratio is the most common technique used to determine the quality of results. It is the ratio between the maximum possible value of a signal and the power of distortion noise(MSE). It is measured in dB’s. A higher value of PSNR indicates a better quality embedding.
### SSIM
SSIM is a metric of comparison to check the similarity between two images. It measures the perceptual difference between the two images. SSIM value close to 1 indicates good quality.
### MSE
Mean Square Error is the averaged value of the square of the pixel-by-pixel difference between the original image and stego-image


## Results
<img src="https://github.com/Divya-Shah/Image-Super-Resolution/blob/main/sample_outputs/1.png" alt="sample_result 1" style="width:80%;"/>
<img src="https://github.com/Divya-Shah/Image-Super-Resolution/blob/main/sample_outputs/2.png" alt="sample_result 2" style="width:80%;"/>
<img src="https://github.com/Divya-Shah/Image-Super-Resolution/blob/main/sample_outputs/3.png" alt="sample_result 3" style="width:80%;"/>

The average SSIM:  0.86

## Conclusion
The implemented approach, SRCNN, learns an end-to end mapping between low- and high-resolution images, with little extra pre/post-processing beyond the optimization. With a autoencoder based architecture, the SRCNN has achieved superior performance than the state-of-the-art methods with average SSIM 0.86. Besides, the implemented structure, with its advantages of simplicity and robustness, could be applied to other low-level vision problems, such as image deblurring or simultaneous SR+denoising, medical image super resolution etc…

## Credits
* A Article from Towards Data Science - [Image Super-Resolution using Convolution Neural Networks and Auto-encoders](https://towardsdatascience.com/image-super-resolution-using-convolution-neural-networks-and-auto-encoders-28c9eceadf90)
* C. K S, R. R. G, S. T N and C. Gururaj, ["Image Super-Resolution Using Convolutional Neural Network,"](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9972459) 2022 IEEE 2nd Mysore Sub Section International Conference (MysuruCon), Mysuru, India, 2022, pp. 1-7, doi: 10.1109/MysuruCon55714.2022.9972459
* Gavrikov, Paul. ["visualkeras."](https://github.com/paulgavrikov/visualkeras/) . (2020).



