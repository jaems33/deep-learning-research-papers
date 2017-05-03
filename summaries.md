##### May 3rd, 2017
### [Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift](https://arxiv.org/abs/1502.03167)
* Perform normalization for each mini-batch
* Problem: Training is complicated by the fact that inputs to each layer are affected by the parameters of the preceding layers so small changes to the network parameters amplify as the network becomes deeper
* When the input distributions to a learning system changes, it is said to be undergoing an internal covariate shift
* Prevents small changes to the parameters from amplifying into larger and suboptimal changes in activations to gradients
* With BN, backprop through a layer is unaffected by the scale of the parameters
* Results in decreasing the requirement of photo augmentation, dropout, L2 regularization, while increasing learning rate and accuracy
* It is applied prior to the non-linearity function
* A differentiable transformation
* I'd like to re-read this when I have a better understanding of math

##### May 2nd, 2017
### [Deep learning with convolutional neural networks for brain mapping and decoding of movement-related information from the human EEG](https://arxiv.org/pdf/1703.05051.pdf)
* Visualizing EEG data using a variety of Deep Networks
* Did not find huge improvements over existing methods (filter bank common spatial patterns, FBCSP) but might be because of the size of datasets, or features might not have enough hierarchical structure that ConvNets could exploit
* Helped by using dropout, batch normalization, and exponential linear units
* Didn't use handcrafted features
* Largely about the potential of ConvNets for EEG-based brain mapping
