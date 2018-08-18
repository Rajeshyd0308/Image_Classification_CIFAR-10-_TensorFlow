# Image_Classification_CIFAR-10-_TensorFlow
Image classification for CIFAR 10 with TensorFlow
<br>
In this notebook I am going to classify images from CIFAR 10 dataset which comprises of Trucks, Airplanes, Cars, Cats and so on.
The image classifer developed is using TensorFlow.
<br>
## Architecture of CNN
The entire model of our conv-net follows conv->conv->pool structure that is every two conv layers are follwed by a pooling layer
The input image fed into the CNN is first fed into
1. Convolution layer comprising of 3x3x3 filters, 16 in number followed by Relu activation.
2. Convolution layer comprising of 3x3x3 filters, 32 in number followed by Relu activation.
3. Max pooling by 2x2 filters with stride 2
    * Dropout Layer
    * Batch normalization layer
<br>
4. Convolution layer comprising of 3x3x3 filters, 32 in number followed by Relu activation.
<br>
5. Convolution layer comprising of 3x3x3 filters, 64 in number followed by Relu activation.
<br>
6. Max pooling by 2x2 filters with stride 2
    * Dropout Layer
    * Batch normalization layer
<br>
7. Flattening 3D output of the previous layer 
<br>
8. Fully connected layer of 256 units followed by Relu activation
    * Dropout Layer
<br>
9. Fully connected layer of 10 units.
<br>
Loss function used is softmax_loss and Update rule Adam

The test set accuracy is 68%
