# FaceKeyPointDetection_Project1
This repository consists of the development of an CNN network for Face Key point detection.

This project is about defining and training a CNN model to perfrom a Face keypoint detection model with computer vision techniques to transform the images.
Facial keypoints (also called facial landmarks) are the small magenta dots shown on each of the faces in the image above. In each training and test image, there is a single face and 68 keypoints, with coordinates (x, y), for that face. These keypoints mark important areas of the face: the eyes, corners of the mouth, the nose, etc. These keypoints are relevant for a variety of tasks, such as face filters, emotion recognition, pose recognition, and so on. Here they are, numbered, and you can see that specific ranges of points match different portions of the face.

## Contents in the repository:
1. **Load and Visualize Data.ipynb :** 
   provides steps to load and vizualize the dataset. The project uses [Youtube Faces dataset] (https://www.cs.tau.ac.il/~wolf/ytfaces/).
  - **Training and Testing Data**
       This facial keypoints dataset consists of 5770 color images. All of these images are separated into either a training or a test set of data.

       3462 of these images are training images, for you to use as you create a model to predict keypoints.
       2308 are test images, which will be used to test the accuracy of your model.
       The information about the images and keypoints in this dataset are summarized in CSV files, which we can read in using pandas. Let's read the training CSV and get the annotations in an (N, 2) array where N is the number of keypoints and 2 is the dimension of the keypoint coordinates (x, y).
  - **Transformation of the Images**
       The images are subjected into preprocessing steps like, Cropping, rescalling, normalizing and converting them to tensor format.
       
    **Results**
    
   ![Trained output](https://github.com/Varun1407/FaceKeyPointDetection_Project1/blob/master/images/Image_1.png)
   
2. **Define the Network Architecture.ipynb :** 
    Defines the CNN network archiecture. 
    This notebook and in models.py, you will:
    1. Define a CNN with images as input and keypoints as output.
    2. Construct the transformed FaceKeypointsDataset, just as before
    3. Train the CNN on the training data, tracking loss
  	4. See how the trained model performs on test data
    5. If necessary, modify the CNN structure and model hyperparameters
    
    **Results**
    
    ![Test_image1](https://github.com/Varun1407/FaceKeyPointDetection_Project1/blob/master/images/image2.png)
    ![Test_image2](https://github.com/Varun1407/FaceKeyPointDetection_Project1/blob/master/images/image3.png)
    ![Test_image3](https://github.com/Varun1407/FaceKeyPointDetection_Project1/blob/master/images/image4.png)
    
 
 3. **Facial Keypoint Detection, Complete Pipeline.ipynb :**
   This notebook provides test and analysis of the trained model:
      1. Detect all the faces in an image using a face detector (we'll be using a Haar Cascade detector in this notebook).
      2. Pre-process those face images so that they are grayscale, and transformed to a Tensor of the input size that your net expects. This step will be similar to the data_transform you created and applied in Notebook 2, whose job was tp rescale, normalize, and turn any iimage into a Tensor to be accepted as input to your CNN.
      3. Use your trained model to detect facial keypoints on the image.
      
    **Results**
    
    ![Unprocessed New Image](https://github.com/Varun1407/FaceKeyPointDetection_Project1/blob/master/images/unprocessedimage.png)
    ![Processed and tested Image](https://github.com/Varun1407/FaceKeyPointDetection_Project1/blob/master/images/processedandtested.png)
      
 4. **Fun with Keypoints.ipynb :**
    This notebook gives an oppurtunity to play around with some funny masks on faces.
    
    **Results**
     ![Funny_Images](https://github.com/Varun1407/FaceKeyPointDetection_Project1/blob/master/images/image5.png)
