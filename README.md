# Brain-MRI-Segmentation-Model-Comparison

Here, we are going to use multiple models(UNET,FPN,RESNET50) on the  same dataset and draw summaries based on their performances.We are going to modify the models to improve their accuracy.To improve our models accuracy we apply Data Augmentation & Data Transformation.So that we can easily avoid overfiting,and also for this our models will learn faster.

## We have 3929 unmasked TIF data to FED our models.
  * Training dataset : 3005 images (76.48%)
  * Validation dataset : 393 images (6.628%)
  * Test dataset : 531 images (13.514%)

## MODELS 
 * UNet:
 
   ![image](https://user-images.githubusercontent.com/41162942/151972104-a51136b8-13f8-47f0-abf2-c679f5e43104.png)
 * FPN :
 
   ![image](https://user-images.githubusercontent.com/41162942/151973501-7f6d30c2-95b6-42f0-ab82-a6a891073637.png)
 * RESNet :
 
   ![image](https://user-images.githubusercontent.com/41162942/151973658-a0d5bfb3-e0ea-4577-9e2c-ad914116847c.png)


## Architecture Comparison

The main difference is that there is multiple prediction layers: One for each upsampling layer.
 Like the U-Net, the FPN has laterals connection between the bottom-up pyramid (left) and 
the top-down pyramid (right).But, where U-net only copy the features and append them, FPN
 apply a 1x1 convolution layer before adding them. This allows the bottom-up pyramid called 
“backbone” to be pretty much whatever you want.

##Accuracy Comparison & Improvement
 * Before:
 
   ![image](https://user-images.githubusercontent.com/41162942/151974330-fb860a4d-adce-42da-be73-249a443872fe.png)
 
 * After:
 
   ![image](https://user-images.githubusercontent.com/41162942/151974403-0856fe0b-a338-4cba-93d3-d756009416e6.png)


