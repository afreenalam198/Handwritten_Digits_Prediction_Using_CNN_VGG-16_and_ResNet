# Predicting Handwritten Digits Between 0-9 using CNNs, VGG and ResNet

## Dataset Description - 

The dataset used for this project is the MNIST Dataset.  
https://en.wikipedia.org/wiki/MNIST_database#:~:text=The%20MNIST%20database%20(Modified%20National,training%20various%20image%20processing%20systems  

The number of data samples included in the dataset is 70,000 (60,000 Train
Set, 10,000 Test Set).  
Each data sample is of 28*28 dimension.  
Labels of this dataset are the 10 handwritten digits from 0-9.  

## Problem Statement -

This dataset (MNIST) is being used to predict handwritten digital numbers between 0-9.  

## Models -

DNN_128 
DNN_256_128 
DNN_2048 
DNN_512_512 
CNN_32_64 
CNN_12_24_32 
VGG_13 
ResNet 

## Dataset Preprocessing -

I first normalized the pixel values (0-255) of the images to the range (0-1) by
converting the integer values into floating point values and then dividing by 255 to scale
the values to the (0-1) range.  
Next, I reshaped the images to have the shape - (-1, 28, 28, 1) to match the expected
input format for conv2D (samples, height, width, channels).  
Lastly, I converted the class labels from integer format to one-hot encoded binary matrix
where each row of the matrix represents a sample, and each column corresponds to a
class. The value 1 indicates that the sample belongs to that class, while 0 indicates
otherwise.  

## Training and Test Split -

The dataset was already split into Train and Test sets (60,000 and 10,000
respectively). I split the Train set randomly into 90% Train and 10% Validation set.  

## Best Performed Models -

The model with the best accuracy is the CNN_12_24_32 architecture for a Learning Rate
of 0.001 with an accuracy of 0.9927.
However, the ResNet architecture has an overall superior performance across the different experimented Learning Rates.  
