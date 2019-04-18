# Image-Caption-Generator-DNNs
A ipynb notebook results in captioning images using Flick8k dataset and Neural Netwiorks


Image Caption Generator
Image caption generator is a model which generates caption based on the features present in the input image. The main goal is to correctly caption the contents of an image so as to be useful to visually impaired people.
Introduction
The basic working of the project is that the features are extracted from the images using pre-trained VGG16 model and then fed to the LSTM model along with the captions to train. The trained model is then capable of generating captions for any images that are fed to it.
Dataset
The dataset used here is the FLICKR 8K which consists of around 8091 images along with 5 captions for each images. If we have a powerful system with more than 16 GB RAM and a graphic card with more than 4 GB of memory, we can try to take FLICKR 30K which has around 30,000 images with captions.

Loading VGG16 model and weights to extract features from the images
The pre-trained weights for the VGG-16 model can be downloaded from [here](https://github.com/fchollet/deep-learning-models/releases/download/v0.1/vgg16_weights_tf_dim_ordering_tf_kernels.h5). The concept of transfer learning is applied here that uses features of the vgg16 model to embed images which is then fed to the LSTM network.

Baseline Model Details:
# Input shape of image tensor (no of samples, features) : (49631, 4096)
# Input shape of text tensor (no of samples, features)
(#samples,vocab_size = 30)
# Output shape of text tensor
(#samples, vocab_size = 30)
# Hyper parameters
Epochs : 6
Batch Size : 32
loss func = categorical_crossentropy
optimizer = adam


# Instructions to run the demo GUI
Install following :
### Dependencies
* Keras
* Tensorflow GPU
* Pre-trained VGG-16 weights
* NLTK
* Matplotlib

### Execution
Run gui gui.py and play around with the UI
### Code
All the code files are attached.
### Video Link
YouTube Link : https://youtu.be/gjSIUrqGits
STEPS:
1.	Download .rar file and unzip it in a directory.
2.	Open command line in the same directory and type following command:
python gui.py
3.	Click on Upload Image button and select any size image to view properly in the demo.
4.	Click on Predict button to view results
