# Music_Generation
Generating Piano music using WaveNet


This repo uses the WaveNet architecture to generate piano music

**WaveNet is a Deep Learning-based generative model for raw audio developed by Google DeepMind**
WaveNet takes the chunk of raw audio wave as input and tries to predict the scuccessive amplitude value as output.

### WaveNet Architecture
The building block of WaveNet is **Casual Dialated 1D Convolution layers**.

**1D Covolutions**
The objective of 1D convolution is similar to the Long Short Term Memory model. It is used to solve similar tasks to those of LSTM. In 1D convolution, a kernel or a filter moves along only one direction.

**Casual 1D Convolutions**
This is defined as convolutions where output at time t is convolved only with elements from time t and earlier in the previous layer.

**Dialated Casual 1D Convolutions**
A *Causal 1D convolution layer* with the holes or spaces in between the values of a kernel is known as Dilated 1D convolution.
The Dialated 1D convolution network increases the receptive field by exponentailly increasing the dialation rate of every hidden layer.

**Residual Block of WaveNet**
Residual and Skip Connections are used thoughout the network to speed up convergence and enable training of much deeper models.

**Workflow of WaveNet**
1. Input is fed into 1D convolutions.
1. The output is then fed to 2 different dilated 1D convolution layers with sigmoid and tanh activations
1. The element-wise multiplication of 2 different activation values results in a skip connection
1. And the element-wise addition of a skip connection and output of causal 1D results in the residual

Read [this](http://tonywangx.github.io/pdfs/wavenet.pdf) and [this](https://medium.com/@satyam.kumar.iiitv/understanding-wavenet-architecture-361cc4c2d623) for more information on WaveNet

Dataset used can be downloaded from [here](https://drive.google.com/file/d/1qnQVK17DNVkU19MgVA4Vg88zRDvwCRXw/view)
