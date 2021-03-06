# Detection of Masked People (from crowd) 
## Overview
When I saw PyImage's Adrian and many Kaggle users taking interest in this kind of a Classifier, I felt it needs to be done on a massive scale.</br>
I made a Classifier that can classify people from a crowd and detect whether they are wearing masks or not. It shows the confidence % upto the accuracy of classification. I web scraped a lot of data for this and it took me a while. </br>
## What did I do
- Went to Kaggle and did some webscraping on different sources,  to construct the dataset
- Performed image augmentation on the dataset
- Fine tuned the hyperparameters of Mobilenet v2 SSDlite that brings the best accuracy without overfitting,used Imagenet weights- https://github.com/chuanqi305/MobileNetv2-SSDLite
- Tested the model

### Scope in future
We can further add Tracking APIs from Computer Vision and use this to track people not wearing masks, which can help the government look for people breaking the law. 

### To try the code:
 ```python3 Detect_image.py --image 1.jpg``` </br>
 ```python3 Detect-Masks-Realtime.py ```
### Output
![1 image](https://github.com/Shaxpy/Robotics-and-AI/blob/master/Mobilenet%20V2/Mask_Classifier/Output/output.jpg)

### Dataset:
For with masks-https://www.kaggle.com/ahmetfurkandemr/mask-datasets-v1,https://www.kaggle.com/vtech6/medical-masks-dataset,https://www.kaggle.com/gooogr/yolo-medical-mask-dataset? and more on Kaggle.</br> 
For without masks-https://www.kaggle.com/abuanas/masked-face-detection-wider-dataset, I used many classes like Demonstration,Group, Cheering, Meeting, Shopper,Dancing, Handshakes etc. 


#### Credits to:
https://www.pyimagesearch.com/2020/05/04/covid-19-face-mask-detector-with-opencv-keras-tensorflow-and-deep-learning/
(He made the code for single masked-person classifier)



