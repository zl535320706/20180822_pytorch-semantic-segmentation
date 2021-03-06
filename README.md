# PyTorch for Semantic Segmentation

1. work well in python 3.6.6 pytorch 0.4.1 tensorflow 1.9 tensorboardX 1.2
2.while training more than 2 days(the lr is 10e-7 in cityscapes-fcn & cityscapes_caffe_vgg and 1e-2 / sqrt(16 / 2) in psp_net),
the pixel acc is 0.5253, the acc_cls is 0.3711, the mean_iu is 0.1847 in datasets "cityscapes"(do not use external training data).
3. and the mean_iu is 0.49151 in datasets "cityscapes" in psp_net. It's not good enough to work as a baseline codes.

This repository contains some models for semantic segmentation and the pipeline of training and testing models,
implemented in PyTorch

## Models
1. Vanilla FCN: FCN32, FCN16, FCN8, in the versions of VGG, ResNet and DenseNet respectively
([Fully convolutional networks for semantic segmentation](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Long_Fully_Convolutional_Networks_2015_CVPR_paper.pdf))
2. U-Net ([U-net: Convolutional networks for biomedical image segmentation](https://arxiv.org/pdf/1505.04597))
3. SegNet ([Segnet: A deep convolutional encoder-decoder architecture for image segmentation](https://arxiv.org/pdf/1511.00561))
4. PSPNet ([Pyramid scene parsing network](https://arxiv.org/pdf/1612.01105))
5. GCN ([Large Kernel Matters](https://arxiv.org/pdf/1703.02719))
6. DUC, HDC ([understanding convolution for semantic segmentation](https://arxiv.org/pdf/1702.08502.pdf))

## Requirement
1. PyTorch 0.2.0
2. TensorBoard for PyTorch. [Here](https://github.com/lanpa/tensorboard-pytorch)  to install
3. Some other libraries (find what you miss when running the code :-P)

## Preparation
1. Go to *models* directory and set the path of pretrained models in *config.py*
2. Go to *datasets* directory and do following the README

## TODO
1. DeepLab v3
2. RefineNet
3. More dataset (e.g. ADE)
