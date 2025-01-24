In this project I used MPLs and CNNs to recognize color images from the CIFAR-10 Dataset.

The CIFAR-10 dataset consists of 60000 colour images in 10 classes, with 6000 images per class, and every image is made by 3 channels (R,G,B) with 32 x 32 pixels.

Dataset is splitted into train, validation and test sets as follow:
<br>• Elements in Train set: 48000
<br>• Elements in Valid set: 2000
<br>• Elements in Test set: 10000

First attempt to images-recogntion with MultiLayerPerceptron (MLP), as a baseline.
A simple MLP with decreasing size of fully connected hidden layers.
Learning rate varies over the epochs, starting with 0.1 and gradually decreasing to about 0.001 at epoch 20
The resulting accuracy on test set equal to 53.4%.
The most misclassified by the model is Cat (accuracy of 33.3%) along with Dog and similarly, Deer with Bird.
While the best classified is Automobile with 66.4%.
Finally, there is an imperfect simmetry among classes, e.g. Cat vs Dog and Dog vs Cat.

Second model with convolutionalNerualNetwork (CNN) with two convolutional layers and a max pooling.
The learning rate varies in the same way as MLP.
Despite a longer training time, the CNN model performed much better than the MLP with a accuracy of 70,4% vs 53,7% on Test set.
Both models have similar tendency to predict worse some classes, such as Cat.
