## Tympanic Membrane Infection Detector

##### Safkan Health | Data Scientist
**Business Problem:** Safkan Health has a headset which users put on to clean their ears. In headsets there is a camera that can take pictures of the inner ear. I built a model to detect Tympanic Membrane Infections. 

**Solution Highlights:** 
  * Developed Deep-CNN model to detect the presence of tympanic membrane infections with 91% accuracy using Tensorflow for the Safkan OtoSet. 
  * Computer Vision methods include localization, CLAHE, transforms
  * Created Production Environment and Deploy ready using Tensorflow Serving  
  * Responsible for the full model pipeline including data acquisition, preprocessing, augmentation, inference, and validation. 

**Write-up:** 

For the development of this Machine Learning system, I was the sole member. I was in charge of the direction and production of each step including the data acquisition, preprocessing, modeling, inference, and more.

Data Preprocessing: The first step of preprocessing is performing Contrast Enhancement on the images. This will normalize issues like lighting, image resolution, and areas of interest. The next step is image segmentation. When trying to detect tympanic membrane infections the most important part is the eardrum. To do this, we apply center of mass based segmentation.

The next step of our pipeline was the Augmentation phase. Data/image augmentation is a process which generates more training data from an existing dataset by manipulating them to create many different versions of the same image. It helps make the classifier more robust as it exposes the classifier to a variety of lighting and color situations and not just generate more images to train.

For this model, we are using Tensorflow. Within Tensorflow, we use the Keras ImageDataGenerator which helps with the Data Augmentation phase. The different augmentations we apply to each image are rotation, width and height shift, shearing, zooming, horizontal and vertical flips, and brightness variance.

Once our images are preprocessed and augmented, we solidify the features we will be using. For this system, we will use the pixel values from the images as features. There are 3 channels per image, representing the RGB spectrum.

The last step before training our Deep Learning model is to normalize the data between the [0, 1] range. Our model architecture is based off of a Convolutional Neural Network. Since we are working with a relatively small dataset, we decide to use transfer learning with the ResNet Model. The ResNet model has been trained on a large image classification dataset and can be fine-tuned to this specific task. Essentially, we can use the already-learned feature maps to generalize to this problem.

The results for the model are 86% test accuracy.


###### All Intellectual Property of this work belongs to Safkan Health and therefore I cannot show any code.


