# 61c-proj4
Optimizing implementation of a pre-trained CNN

Introduction/Background
In this project, you will apply some of the performance optimization techniques that you have learned in class to the real-world problem of classifying images using a Convolutional Neural Network (CNN). 
The following sections will introduce you to CNNs and a high-level idea of what is going on.

How does a Computer tell a Cat from a Chair?
Image classification describes a problem where a computer is given an image and has to tell what it represents (usually from a set of possible categories). Image classification has long been considered a difficult challenge, and a lot of work has been done over the years to improve its accuracy (i.e., what fraction of pictures gets classified correctly).

Lately, Convolutional Neural Networks (CNNs) have emerged as a promising solution to this problem. In contrast to classical algorithms, which explicitly encode some insight about the real world into a function, CNNs instead learn a function by being presented with a large number of examples and adjust themselves based on these examples -- this process is called training. Once the CNN has learned the function (or to be more precise, an approximation of it), it can repeatedly apply it to inputs it has not seen before.

How do Convolutional Neural Networks Work?
For this project, we do not require you to understand how CNNs work in detail. However, we want to give you enough information to get a sense of the high-level concepts. If you would like to learn more, we encourage you to take one of the Machine Learning or Computer Vision classes in the department, or check out this brief online-course.

At a high level, a CNN consists of multiple layers. Each layer takes a multi-dimensional array of numbers as input and produces another multi-dimensional array of numbers as output (which then becomes the input of the next layer). When classifying images, the input to the first layer is the input image (i.e., 32x32x3 numbers for 32x32 pixel images with 3 color channels), while the output of the final layer is a set of likelihoods of the different categories (i.e., 1x1x10 numbers if there are 10 categories).

Each layer has a set of weights associated with it -- these weights are what the CNN "learns" when it is presented with training data. Depending on the layer, the weights have different interpretations, but for the purpose of this project, it is sufficient to know that each layer takes the input, performs some operation on it that is dependent on the weights, and produces an output. This step is called the "forward" pass: we take an input and push it through the network, producing the desired result as an output. This is all that needs to be done to use an already trained CNN to classify images.

Your Task:
In this project, we give you a pre-trained CNN that can classify 32x32 images into 10 categories (such as dog, cat, car or plane). Using this CNN, we develop an application that takes a large set (i.e., 1000's) of images as input and finds those that contain cats. This CNN has been trained on the CIFAR-10 data set, which consists of 50,000 32x32 images showing 10 different categories. The network consists of 11 layers, each performing a particular operation on a specific size of input, producing a specific size of output. Throughout the project, you can assume this specific network with the provided weights.
Unfortunately, our initial implementation is very slow -- your job is to make it faster!
