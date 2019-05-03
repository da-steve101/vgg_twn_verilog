# vgg_twn_verilog

A hardware design to classify CIFAR10 images

This package uses [twn_generator](https://github.com/da-steve101/twn_generator)

The architecture implemented is as follows:

| Layer   | Output Size  |
| ------- | ------------ |
| input   | 32x32x3      |
| conv1   | 32x32x64     |
| BNRELU  | 32x32x64     |
| conv2   | 32x32x64     |
| BNRELU  | 32x32x64     |
| MP1     | 16x16x64     |
| conv3   | 16x16x128    |
| BNRELU  | 16x16x128    |
| conv4   | 16x16x128    |
| BNRELU  | 16x16x128    |
| MP2     | 8x8x128      |
| conv5   | 8x8x256      |
| BNRELU  | 8x8x256      |
| conv6   | 8x8x256      |
| BNRELU  | 8x8x256      |
| MP3     | 4x4x256      |
| dense   | 128          |
| BNRELU  | 128          |
| softmax | 10           |
