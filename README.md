# SVM
Image Classification using HOG for features extraction, and SVM for classification between weeds and corn

Simple image classification algorithm in python using SVM for classification and HOG for features extracion on RGB images.

<img src="https://user-images.githubusercontent.com/60111412/86513939-d3c9d800-be16-11ea-98cd-45971fd4b402.png" width="400"/>

HSV based Color Segmentation is applied for improving accuracy.

<img src="https://user-images.githubusercontent.com/60111412/86513940-d88e8c00-be16-11ea-94a1-afba6c4ec347.png" width="400"/>

Each obejcts (weed or corn) was extracted from a PASCAL VOC format file using coordinates and label.

Here is an example of a Broadleaves weed extracted from the image 

<img src="https://user-images.githubusercontent.com/60111412/88196627-16c6e080-cc4a-11ea-8095-7ca2e53f5e84.png" width="600"/>

After the objects extraction, Features Extraction was preformed by extracting each object HOG (Hisotgram Of Gradients), giving us the 
size and direction of the gradients in the image which implies on ROI's (Regions Of Interest).

<img src="https://user-images.githubusercontent.com/60111412/88197211-d1ef7980-cc4a-11ea-9725-3aeaa4754fe1.png" width="600"/>


The objects are extracted from the images using XML files. Overall there are 118 images and ~33000 objects of corn and weeds.
The train-tesst ratio is 70%-30% respectively.

First, we trained the SVM model with the scikit-learn default parameters.
The model produced 90% for both Accuracy and F1-Score.

For better results, we used the scikit-learn optimization tools GridSearchCV, which enable us to 
look for the best model's Hyper-Parameters.

After tuning the model, we improved the results which can be seen in the next Confusion Matrix:

<img src="https://user-images.githubusercontent.com/60111412/88200844-5d6b0980-cc4f-11ea-9718-2ec4cfebfe6c.png" width="600"/>

