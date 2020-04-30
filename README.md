# HackerEarth Prize Competition- Detect emotions of your favorite toons

This is a competition that was hosted on HackerEarth and last submission date was May 1st, 2020.

## Description

### **Problem statement**

The International Day of Happiness is celebrated globally on March 20 every year with an objective to promote happiness and well-being as a fundamental human right for all. On this International Day of Happiness, we are bringing back all the joy and happiness for you. This fun challenge requires you to build a model that detects emotions of your favorite characters of the iconic toon show—Tom and Jerry.



The dataset consists of the following two columns:

    Column Name 	Description
    Frame_ID        Indicates the frame of the video in .jpg format
    Emotion	    Emotion label: angry, sad, happy, surprised, Unknown

### **Data description**
The dataset contains two video files and two .csv files. These files perform the following tasks:


> Train Tom and jerry.mp4: Video file used for training
> Train.csv: Contains human-generated labels for 298 frames [FrameRate=5] from the training video
> Test Tom and jerry.mp4: Video file to detect emotions on the face
> Test.csv: Contains 186 frames [FrameRate=5] from the test video in .csv format


sample_submission

    Frame_ID,Emotion
    test0.jpg,happy
    test1.jpg,happy
    test2.jpg,happy
    test3.jpg,happy
    test4.jpg,angry
    test5.jpg,unknown

### **Evaluation metric**

    score = 100 * f1_score ( actual_values, predicted_values, average = 'weighted' )

Note: To avoid any discrepancies in the scoring, ensure all the index column ('Image_File') values in the submitted file match the values in the provided **test.csv** file.

[Competition Link](https://www.hackerearth.com/challenges/competitive/hackerearth-deep-learning-challenge-emotion-detection-tom-jerry-cartoon/machine-learning/detect-emotions-of-your-favorite-toons-7d2c0f23/)

## My understanding of the competition

It is Classification problem with metric evaluation as f1_score. ResNet50 which is a Pre-trained classification architectures has been used as a base model. And upon it, a pretrained VGG19 model has been used that works fine on this dataset, with suitable data augmentations and regularizations. Hoping for a easy solution as this was my first attempt. 

## My approach

1. Create train and test image datasets from their given respective train and test videos. 
1. Check the class distribution of imbalances.
2. Training Images Viualization.
3. Image Shape Variations to set the resize values.
4. Creating Folders for Dataset.
5. Normalization Parameter.
6. performed augmentation on the dataset.
7. Train the model with Adam optimizer. 
8. Saving best checkpoints based on best achieved validation score.
9. Prediction on the trained model.

## Files
1. [Ipynb notebook](https://github.com/ayush1427/Detect-emotion-of-your-favourite-toons/blob/master/My-approach.ipynb) 


## Contributions 
Any improvements to my method, including changes, typos, etc. would be greatly appreciated.
