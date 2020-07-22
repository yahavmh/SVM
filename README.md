# SVM
Image Classification using HOG for features extraction, and SVM for classification between weeds and corn

Simple image classification algorithm in python using SVM for classification and HOG for features extracion on RGB images.

<img src="https://user-images.githubusercontent.com/60111412/86513939-d3c9d800-be16-11ea-98cd-45971fd4b402.png" width="400"/>

HSV based Color Segmentation is applied for improving accuracy.

<img src="https://user-images.githubusercontent.com/60111412/86513940-d88e8c00-be16-11ea-94a1-afba6c4ec347.png" width="400"/>

The objects are extracted from the images using XML files. Overall there are 118 images and ~33000 objects of corn and weeds.
The train-tesst ratio is 70%-30% respectively.

Each obejcts (weed or corn) was extracted from a PASCAL VOC format file using coordinates and label.

Here is an example of a Broadleaves weed extracted from the image 

<img src="https://user-images.githubusercontent.com/60111412/88196627-16c6e080-cc4a-11ea-8095-7ca2e53f5e84.png" width="400"/>


