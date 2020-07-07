The above code is the implementation of the paper https://arxiv.org/pdf/1608.02164.pdf , the code involves the implementation using the pretrained model of VGG16,
the libraries of numpy, scipy and sklearn have been utilized to complete the implementation.

The basic structure of the code is as follows,
1) We get the similarity matrix and the image dataset used in the paper from the authors github profile.
2) We make the pretrained model ready by removing the last fully connected layer.
3) The images are preproccesed and are fed to our model, we store the obtained features.

