# Monkey Classification

The aim of this model is to classify images of monkeys into one of ten species. This will be a fine-grained classifier as it is aimed at differentiating between very similar objects, rather than very separate classes of object.

The data or functinoality from this model are not particularly useful, this project is mainly focused on developing and understanding the method for creating a fine-grained classifier. These skills will be applicable to more industrially useful classifiers that I may develop in future.

## DATA

The dataset consists of pre-labelled images of monkeys. The dataset consists of two files, training and validation. Each folder contains 10 subforders labeled as n0~n9, each corresponding a species form Wikipedia's monkey cladogram. Images are 400x300 px or larger and JPEG format (almost 1400 images).

This dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/slothkong/10-monkey-species/data). This dataset was constructed by pulling google search results for each of the monkey species.

The dataset consists of two files, training and validation. Each folder contains 10 subforders labeled as n0~n9, each corresponding a species form Wikipedia's monkey cladogram. Images are 400x300 px or larger and JPEG format (almost 1400 images).

## MODEL 

The model is a CNN looselybased on the AlexNet architecture. It consists of two layers of Convolution-ReLU-MaxPooling, followed by a Convolution-ReLU-MaxPooling-Dropout (Dropout is included during training to reduce overfitting). This is finally flattened into two fully-connected layers.

## HYPERPARAMETERS

The primary hyper-parameters of the mode are:

-**Learning rate**
-**Image size** (The images in the training set are all of different resolutions, so had to be scaled to a uniform size to train the model. An optimal size was found to balance training cost and information loss of downscaling.)
-**Batch size**

## RESULTS

The model achieved an accuracy of around 75%, with some species achieving a very high idnetification rate of 95%.

![Confusion Matrix](conf.png)

![Performance by species](perf.png)
