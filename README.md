# CIFAR-10-ResNet


Input Image: 32x32

Initial Convolution (Gold):

Kernel Size: 3x3

Filters: 16

Output Feature Map Size: 32x32x16

The image is convolved with 16 filters of size 3x3.


## Residual Blocks

### Blue Residual Block:

**Four Convolutional layers:**

Kernel Size: 3x3

Filters: 16

Each convolution is followed by Batch Normalization and ReLU activation.

Output Feature Map Size: Remains 32x32x16

### Green Residual Block:

**First Layer:**

Kernel Size: 3x3

Filters: 32

Stride: 2 (Downsampling)

Output Feature Map Size: 16x16x32 (halved spatial dimensions, increased depth)

Downsampling is achieved by using a stride of 2, reducing the spatial dimensions from 32x32 to 16x16.

**Subsequent Layers:**

Kernel Size: 3x3

Filters: 32

Output Feature Map Size: 16x16x32

The remaining convolutions keep the same spatial size but change the depth of the feature maps.


### Red Residual Block:

**First Layer:**

Kernel Size: 3x3

Filters: 64

Stride: 2 (Downsampling)

Output Feature Map Size: 8x8x64 (again halving spatial dimensions, increasing depth)

Another downsampling layer further reduces the spatial dimensions to 8x8 while increasing the number of feature maps to 64.

**Subsequent Layers:**

Kernel Size: 3x3

Filters: 64

Output Feature Map Size: 8x8x64
