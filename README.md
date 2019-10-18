# Mask_Rcnn_Segmentation 

you can follow this link also : https://www.analyticsvidhya.com/blog/2019/07/computer-vision-implementing-mask-r-cnn-image-segmentation/


I am fascinated by self-driving cars. The sheer complexity and mix of different computer vision techniques that go into building a self-driving car system is a dream for a data scientist like me.

So, I set about trying to understand the computer vision technique behind how a self-driving car potentially detects objects. A simple object detection framework might not work because it simply detects an object and draws a fixed shape around it.

That’s a risky proposition in a real-world scenario. Imagine if there’s a sharp turn in the road ahead and our system draws a rectangular box around the road. The car might not be able to understand whether to turn or go straight. That’s a potential disaster!

Instead, we need a technique that can detect the exact shape of the road so our self-driving car system can safely navigate the sharp turns as well.

The latest state-of-the-art framework that we can use to build such a system? That’s Mask R-CNN!

So, in this article, we will first quickly look at what image segmentation is. Then we’ll look at the core of this article – the Mask R-CNN framework. Finally, we will dive into implementing our own Mask R-CNN model in Python. Let’s begin!


Step 1: Clone the repository

First, we will clone the mask rcnn repository which has the architecture for Mask R-CNN. Use the following command to clone the repository:

git clone https://github.com/matterport/Mask_RCNN.git

Once this is done, we need to install the dependencies required by Mask R-CNN.

 
Step 2: Install the dependencies

Here is a list of all the dependencies for Mask R-CNN:

    numpy
    scipy
    Pillow
    cython
    matplotlib
    scikit-image
    tensorflow>=1.3.0
    keras>=2.0.8
    opencv-python
    h5py
    imgaug
    IPython

You must install all these dependencies before using the Mask R-CNN framework.

 
Step 3: Download the pre-trained weights (trained on MS COCO)

Next, we need to download the pretrained weights. You can use this link to download the pre-trained weights. These weights are obtained from a model that was trained on the MS COCO dataset. Once you have downloaded the weights, paste this file in the samples folder of the Mask_RCNN repository that we cloned in step 1.

 
Step 4: Predicting for our image

Finally, we will use the Mask R-CNN architecture and the pretrained weights to generate predictions for our own images.

Once you’re done with these four steps, it’s time to jump into your Jupyter Notebook! We will implement all these things in Python and then generate the masks along with the classes and bounding boxes for objects in our images.
