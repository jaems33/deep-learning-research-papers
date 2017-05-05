##### May 4th, 2017
### [Learning to Estimate 3D Hand Pose from Single RGB Images](https://arxiv.org/abs/1705.01389)
* [Github Repo](https://github.com/lmb-freiburg/hand3d)
* This was a real fun one to experiment with
* In summary, they created a network that took 2D images, identified hand gestures, and created 3D models of the hand based on a priori knowledge
* They complement their dataset with 3D models with animations 
* They augment the training images by altering the lighting in the 3D renders, adjusting the quality of exported JPGs, and specular reflections on the skin
* All samples came with a 21 keypoint skeleton model of the hand, and 33 segmentation masks
* The image goes through a network consisting of hand segmentation, crop and resize, PoseNet(localizes hand keypoints), and then PosePrior(estimates most likely 3D structure)
* Able to also detect which hand orientation and gesture
* Still seems up to optimization as their error rate was marginally better than the comparison they offered, but unlike the comparison, they didn't have 3D to work with from 2D RGB inputs

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
