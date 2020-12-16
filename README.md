### This repo is still under development.  

## Overview

Automatic Optical Inspection(AOI) is a machine embedded in Printed Circuit Board Assembly(PCBA) process.  AOI uses a multi-camera system to scan automatically the PC board and compare the scanned image with a database for the purpose of finding defects.  Its high speed has become one of the crucial factor for the advancement of Surface Mount Technology.

![SMT Line with AOI location]() 
Source: 

The defects that can be detected by an AOI machine are several, just to provide a very short list of common problems: components missing, lift, gap at tail end, shift and wrong polarity. 

![Defect images]()
Source: 

To be qualified as AOI equipment operator, he/she needs to receive a solid training on setting and manipulating the parameters of dozens or even hundreds of the features and functions available in the machine.  In addition, AOI operators needs to co-work with other members of PCBA team to work on proper resolution of the generated faulty parts, receive feed-back for improvements and risks mitigation.

The hardest part of an AOI operator's day-to-day responsibility, in my opinion, is the AOI initial setup that operator's needs to go through each time there is a new PCB model to be manufactured.  In general, this complex setup may take from 2 to 8 hrs, depending on the quantity of components in the PCB.

With the on going great leap improvement in Computer Vision(CV) and Machine Learning(ML), especially Deep Learning(DL), techniques and accuracy, it is only a matter of time that we incorporate them into AOI equipment.  This repo has as objective to start providing some of this work, by first creating synthetic images for training neuron networks and then reproducing some basic AOI functionalities.

Finally, the purpose to use synthetic images.  Real images on defective boards are rare.  In a typical PCBA line, operators seldom keep images, perhaps few are kept for follow-up analysis.  In addition, the images generated by AOI are not immediately discarded, but kept in one of the connected computer hard disk.  We can use these images for training, but they are unlabeled.  Therefore, given these situations, I decided to create synthetic images as I did in my [past work]() to mitigate these problems. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

Generate synthetic images for:
* Detection of component shift.
* Pretraining model.

Features:
- [] Detect different components types. 
- [] Find component sizes.
- [] Detect and recognize characters(parts numbers) printed on components, recognition at different rotation and different character types. 
- [] Metrics to compare the performance of synthetic vs real images.  Connect with Weights and Biases. 

 
|Detectron2|Method|Backbone|Hardware|LR Scheduler|Train Time|Train Memory|Inference Time|Box AP|Mask AP|
| :---: | :---: | :---: | :---: | :---: |  :---:  |  :---:  |  :---:  |  :---:  |  :---:  | 
|[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chho-work/AOI/blob/master/nb/AOI_Detectron2_MaskRCNN.ipynb)|ResNet50|MaskRCNN|GPU|3x|xx/s|xx|xx/s|xx|xx.xx|


## Reference:
* Image Sources:
	


