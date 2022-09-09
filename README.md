# Image Classification for a City Dog Show

## AIM

The aim of this project is to use a pre-trained image classifier to identify dog breeds with specific focus on the use 
of Python and not on the actual classifier. The code was executed in jupyter notebook for ease of communicating results.

## Description:
The project was designed based on this case study:

A city is hosting a citywide dog show and I have volunteered to help the organizing committee with contestant registration.
Every participant that registers must submit an image of their dog along with biographical information about their dog.
The registration system tags the images based upon the biographical information.

Some people are planning on registering pets that aren’t actual dogs.

I need to use an already developed Python classifier to make sure the participants are dogs.

## Key Tasks:
1. Using Python skills, determine which image classification algorithm works the "best" on classifying images as "dogs" or "not dogs".

2. Determine how well the "best" classification algorithm works on correctly identifying a dog's breed.

3. Time how long each algorithm takes to solve the classification problem. With computational tasks, there is often a trade-off between accuracy and runtime. 
The more accurate an algorithm, the higher the likelihood that it will take more time to run and use more computational resources to run.

## Objectives
1. To Correctly identify which pet images are of dogs (even if breed is misclassified) and which pet images aren't of dogs.
 
2. To Correctly classify the breed of dog, for the images that are of dogs.
 
3. To determine which CNN model architecture (ResNet, AlexNet, or VGG), "best" achieve the objectives 1 and 2.
 
4. To consider the time resources required to best achieve objectives 1 and 2, and determine if an alternative solution would have given a "good enough" result, given the amount of time each of the algorithms take to run.

## Note:

To simplify isssues, the image classifier is simply looked at as a tool that has an input and an output. The Input is an image. The output determines what the image depicts. (for example: a dog). 
Also note that image classifiers do not always categorize images correctly, this gets better based on some parameters. 

For this image classification task, an image classification application using a deep learning model called a convolutional neural network (often abbreviated as CNN) was used. 
CNNs work particularly well for detecting features in images like colors, textures, and edges; then using these features to identify objects in the images. 
The CNN used has already learned the features from a giant dataset of 1.2 million images called ImageNet. 
There are different types of CNNs that have different structures (architectures) that work better or worse depending on your criteria.

With this project I explored three different architectures (AlexNet, VGG, and ResNet) and determined which is best for the application.

A classifier function in classifier.py was provided, this allowed the use of the CNNs to classify the images easily. The test_classifier.py file contains an example program that demonstrates how to use the classifier function. 
For this project, I focused on using my Python skills to complete these tasks using the classifier function. I explained in another repository how the classifier was built.

Please note that certain breeds of dog look very similar. The more images of two similar looking dog breeds that the algorithm has learned from, the more likely the algorithm will be able to distinguish between those two breeds.

We have found the following breeds to look very similar: Great Pyrenees and Kuvasz, German Shepherd and Malinois, Beagle and Walker Hound, amongst others.


## Results
In this section we provide the results from running the check_images.py for all three CNN model architectures: 

The program produced the results when run_models_batch.sh (or run_models_batch_hints.sh) in the Printing Results section was run.

Discuss how the check_images.py addressed the four primary objectives of this Project

In this project we had 2 main objectives:

Identifying which pet images are of dogs and which pet images aren't of dogs
Classifying the breeds of dogs, for the images that are of dogs
Your program should have provided you with objectives 1 and 2 when it was run. In the table below, you will find our results for each of the model architectures. Your program should provide you with the same results as we have provided below.

1. For objective 1, notice that both VGG and AlexNet correctly identify images of "dogs" and "not-a-dog" 100% of the time.
2. For objective 2, VGG provides the best solution because it classifies the correct breed of dog over 90% of the time.


Given our results, the "best" model architecture is VGG. It out performed both of the other architectures when considering both objectives 1 and 2. You will notice that ResNet did classify dog breeds better than AlexNet, 
but only VGG and AlexNet were able to classify "dogs" and "not-a-dog" at 100% accuracy. The model VGG was the one that was able to classify "dogs" and "not-a-dog" with 100% accuracy and had the best performance regarding breed classification with 93.3% accuracy.

To run the test files:
Use sh run_models_batch_uploaded.sh 
