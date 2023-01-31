# fish-species_classification

## About
- Created a DeepLearning model to classify the fish image to the species it belongs.
- The model is trained to classify 15 local fish species.
- This model can be integrated with a mobile app, helpful for people to identify the species of fish without any help.

Table of contents
=================

<!--ts-->
   * Data creation
   * Prepare data
   * Model buliding

## Dataset
- Dataset is created manually,by visiting local fish markets and collecting images.
- It has around 500 images only, this number and kinds of images is very small to train the model. because the less data you have, the less chance you have of getting accurate predictions for data that your model hasn't yet seen. So that I decide to use Image Augmentation.
- Augumentation techniques are performed to the data to increase the size of data, so that the model can be trained well.

Image Augmentation: amends the images on-the-fly while training using transforms like rotation, shifting, brightness. and it is a way to avoid overfitting the data.

## Preparing the data
- After all the species are augumented it has to be split to train and est folders to bulid the model.
- 'splitfolders' library has been used and train-test split ratio of 8:2 is given.

## Model
- A Neural Network is build to extract the feactures and the model learns from the features to classify the future images.
- The model is build with one input layer, 3 hidden layers and a output layer.
- In the input layer, the input of size (256 x 256) is given and of 3 channels as for classifying fishes the color of fish is an important feature.
- In the Dense layer, relu activation function is used, as it helps to prevent the exponential growth in the computation required to operate the neural network.
- In the output layer, softmax activation function is used.And this layer contains 15 units (15 kinds of species are to be classified).

<!-- ## Requirements

Python 3.7 or later with all [requirements.txt] 

To install run

```
$ conda create -n admin python=3.7 --yes
$ pip install -r requirements.txt
```
-->

## Contributing
Pull requests are welcome !

1. Create your feature branch: `git checkout -b my-new-feature`
2. Commit your changes: `git commit -m 'Add some feature'`
3. Push to the branch: `git push origin my-new-feature`
4. Submit a pull request to Dev Branch
5. The maintainer would review the changes  and merge it to Dev branch for testing.

For major changes, please open an issue first to discuss what you would like to change.

