# Project - Udacity Data Scientist Nanodegree Capstone: Dog Breed Classifier

## Project Overview
In this project, we applied Convolutional Neural Networks (CNNs) and transfer learning in order to build a pipeline that processes user images.

1. Convolutional Neural Networks (CNNs) are commonly used to analyse image data. 
2. Transfer learning is a technique that allows to reuse a model across different tasks. 

The objective is to identify an estimate of the dog's breed using a classification algorithm, given it is provided an image of a dog. If given an image of a human, the code will identify the resembling dog breed. If the algorithm can't identify the image as a human or dog, it will say so. This use case is a fun exercise for anyone getting started with image classification. 

Feel free to read about the project in this [Medium](https://medium.com/@hoangnym/udacity-dog-breed-classification-capstone-project-477093db40ff) blog entry.

## Table of Contents
1. [Motivation](#motivation)
2. [File Structure](#file_structure)
3. [Instructions](#instructions)
4. [Acknowledgements](#acknowledgements)
5. [Content](#content)
6. [Findings](#findings)
7. [Authors](#authors)

<a name="motivation"></a>

### Motivation
In this project, Udacity in collaboration with Figure Eight provides a data engineering project. The goal was to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages and use Flask to visualize the data.

<a name="file_structure"></a>

### File Structure
    .
    ├── saved_models     
    │   ├── weights.best.from_scratch.hdf5  # trained model built from scratch
    │   └── weights.best.inception.hdf5     # trained model using inception weights
    │   └── weights.best.VGG16.hdf5         # trained model using VGG16 weights
    ├── haarcascades                   
    │   ├── haarcascade_frontalface_alt.xml # XML file for use with the OpenCV face detector class
    ├── images                              # images used to test the algorithm's predictions
    ├── dog_app.html                        # jupyter notebook saved in html format
    ├── dog_app.ipynb                       # jupyter notebook saved in ipynb format
    ├── extract_bottleneck_features.py      # python script with provided functions
    ├── LICENSE.txt                         # license text
    ├── CODEOWNERS                          # owners of the code
    └── README.md


<a name="instructions"></a>

### Instructions
1. Open the html or ipynb file in order to go through the analysis yourself or play around with it.
2. Download bottleneck_features files from step 5 in dog_app.html file
3. Recreate the project following the steps outlined under [Content](#content)

<a name="acknowledgements"></a>

### Acknowledgements
- [Udacity](https://www.udacity.com/) for providing the efforts in the Data Science Nanodegree Program and enabling me to build an image classification model


<a name="content"></a>

### Content
Introduction
Step 1: Import datasets provided by Udacity
Step 2: Detect humans
Step 3: Detect dog
Step 4: Create a CNN from scratch to Classify Dog Breeds
Step 5: Create a CNN using transfer learning to Classify Dog Breeds
Step 6: Write and test algorithm


<a name="findings"></a>

### Findings
- The inception model achieved a test accuracy of 79%, which is above the 41% accuracy using the VGG16 model.
- Training a model from scratch delivers great insights for beginners
- The output is better than expected. It managed to identify dog pictures as dogs and pictures of humans as humans.

Three points of improvement for the algorithm:

- The model needs to be able to pick up subtle differences between similar breeds. Some of them have similar colors and shapes but differ in size and posture, as the case between an Irish and an American Water Spaniel.
- There is more variety needed concerning the type of breeds the model predicts for humans. For instance, J.Bezos and B.Gates are predicted the same breeds, even though I clearly look different.
- I think the model could use some improvements on its ability to classify pictures with noise (blurry backgrounds, white backgrounds, etc.). It needs clear images, otherwise the model always give you similar predictions.


<a name="authors"></a>

### Authors
- [Minh Hoang Nguyen](https://github.com/justZen94)
