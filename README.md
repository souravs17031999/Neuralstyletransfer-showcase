# Project Objective: 
## This project aims to acheive neural style transfer using the algorithm given by Paper [Image Style Transfer Using Convolutional Neural Networks by Gatys](https://arxiv.org/pdf/1508.06576.pdf), implemented in Pytorch.


# Theory and basic overview :
### Basics of CNN : 
Convolutional neural networks (CNN) are class of deep neural networks but differs from basic MLP (multi layer perceptron) in a way that unlike MLP , where all the neurons of the previous layers are connected to all the layers of next layers and this unnecessarily increases number of parameters whereas in CNN , at each layer only some of the neurons are connected to next layers , the neurons which are important to preserve the spatial information.
As we can see in the below picture how CNN's help in preserving spatial informative , as how these neurons are interconnected in 2D and thus helps in identifying patterns , relations among different parts of a image.

![](pics/cnn.JPG)

Hence, helping in extracting features , and also called feature extractors.

This works on the idea of mathematical operation called **convolution** , in simple words it is simply superimposing one function over the other and here also , we are masking the image with matrices known as **"kernels"** or **"filters"** and the results produced are called **"feature maps"**.

![](pics/cnnneural.gif)

This graphics illustrates under the hood calculation of different feature maps which then combines over all the channels (1 for gray scale images and 3 for RGB images) produces the final result.
We can detect edges, contours based on the results of feature maps produced as sudden change in light intensity pixels confirms there is a edge so there values in features maps will signifactly differ around that region.

### Content and Style images
So, now we know how to extract features from a image using CNN.
Now, we are going to see what are content images and style images which we will be using in our algorithm to generate some new awesome artistic images.

**Content images** : images from which we are going to extract contours, borders, edges.

![](pics/contentextract.png)


![](pics/neural.gif)
