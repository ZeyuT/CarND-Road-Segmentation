# noise2self-Implementation

## General Information
A simple implementation of [noise2self](https://arxiv.org/abs/1901.11365), using Python and keras/tensorflow.

The denoising model is a small scale U-Net. A convolution-based masking process is applied to the image data and makes the model prediction $J-invariant$ as stated in the paper.

MNIST and fashion MNIST are used for assessing the denoising model under the framework proposed in the paper. Guassian noise is added to images in both datasets to generate noisy datasets.

Details of implementation are included in the project phase 2 report.

## Get started
The whole procedure is inlcuded in `noise2self.py`. 

To run the training, testing process and get some output image examples:
```shell
python3 noise2self.py
````
Optional arguement: \\
`--dataset`: mnist, fashion-mnist;  \\
`--num-batches`: positive number; \\
`--batch-size`: positive number;  \\
`--num-examples`: positive numbers; \\
`--show-loss-plot`.

Function files are in folder `src`: \\
`marker.py`: implement masking procedure; \\
`model.py`: construct a small-scale U-Net model;  \\
`noise.py`: add gaussian noise to images in raw datasets; \\
`utils.py`: some help functions for plotting results. 

## Dependencies
numpy>=1.16 \\
tensorflow>=1.13.1  \\
matplotlib  \\
Keras
