The above code is the implementation of the paper https://arxiv.org/pdf/1608.02164.pdf , the code involves the implementation using the pretrained models of VGG16 and Alexnet, the libraries of numpy, scipy and sklearn have been utilized to complete the implementation.

The basic structure of the code is as follows,
1) We get the similarity matrix and the image dataset used in the paper from the authors github profile.
2) We make the pretrained model ready by removing the last fully connected layer.
3) The images are preproccesed and are fed to our model, we store the features obtained in a matrix let us call it F.
4) This matrix, F is of size 120 x no. of features (say n), it is then multiplied with it's transpose to form a 120 x 120 matrix (FF').
5) This 120 x 120 matrix is then compared with the 120 x 120 human similarity matrix in terms of correlation coefficient.
6) Now we will modify the weightage of these different features from the n features we have, by having a diagonal matrix W. This matrix is obtained from performing Ridge Regression to the features and then comparing with the human similarity matrix.
7) This is basically changing FF' to FWF' where W is obtained by performing ridge regression. Also Grid Search is used to find the most suitable hyper-parameter for Ridge regression.
8) After this process we compare the new similarity matrix obtained and the human similarity matrix in terms of correlation coefficient.

