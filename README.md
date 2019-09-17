# Introduction
This repository contains my own implementation of the MobileNet Convolutional Neural Network (CNN) developed in Python programming language with Keras and TensorFlow enabled for Graphic Processing Unit (GPU). The provided source-code contains two functions representing the implementations of the MobileNetV1 and MobileNetV2 architectures. A case study in a image set of two airplane models is also provided to evaluate the performance of the network.

## Case study
A MobileNetV1 network was developed to identify images of the airplane models Airbus A320 and Boeing 737. A dataset with over 2000 images of each airplane model was created to train the CNN model. Another dataset with over 300 images of each airplane model was also create to validate the performance of the network.

The training dataset contains 2442 images of the Airbus A320 model and 2309 images of the Boeing 737. The validation dataset contains 487 images of the Airbus A320 and 335 images of the Boeing 737. Therefore, 4751 images were used for training the model and 822 images were used for validation.

**Obs: Unfortunately it is not possible to provide the images used in the training and validation of the network due to the Copyright policy. However, the trained model is available for further refinement.**

## Experiments
The model was developed in the Python programming language with the following libraries:

**Keras: version 2.2.5
**TensorFlow: version 1.14.0
**Platform: Google Colab

The CNN model was built with the following configuration:

**Batch size: 32**
**Epochs: 200**
**Optimizer: Adam**
**Learning rate: starting from 0.001
**Width multiplier: 1
**Resolution multiplier: 1

The learning rate starts in 0.001. If no improvement in the validation loss is obtained after 10 epochs, the learning rate is reduced by a factor of 0.7. The minimum value of the learning rate was set to 0.0001. The width multiplier represents the factor by which the number of filters is reduced when the images flow through the network layers. In general, values between 0.5 and 1 are assigned to the width multiplier. The resolution multiplier is used to reduce the resolution of the input images. The reader are invited to see more information about the hyperparameters of the MobileNetV1 model in the original paper available in [arXiv.org](https://arxiv.org/pdf/1704.04861.pdf).

### Training and validation loss
The following plots depict the training and validation loss resulting from the training process of the MobileNetV1 model.

![accuracy_mbnet_v1](https://user-images.githubusercontent.com/39133414/65028039-c12af480-d911-11e9-9078-083182ba3fcf.jpg)

![loss_mbnet_v1](https://user-images.githubusercontent.com/39133414/65028041-c1c38b00-d911-11e9-8cb4-45c57b696910.jpg)

The network stabilized after 50 epochs as can be seen in the above pictures. The following images depict the performance of the trained model in images not beloging to the validation set.



## Future works
