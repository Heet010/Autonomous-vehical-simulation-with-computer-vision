Autonomous Vehicle simulation with Computer Vision
This repo contains code for predicting steering angles of self driving car. The inspiraion is taken from Udacity Self driving car module as well End to End Learning for Self-Driving Cars module from NVIDIA, and inspired from 'AI-Driver-CNN-DeepLearning-PyTorch' by milsun.

The End to End Learning for Self-Driving Cars research paper can be found at (https://arxiv.org/abs/1604.07316) This repository is built on PyTorch library.

Abstract
Data contains 3 camera(left, centre, right) output images as inputs along with steering angle as labels. Task is a supervised machine learning problem where objective is to predict steering angle based on camera inputs.

Here, CNN based architecture is used, which comprises of 5 Convolutions layers followed by a fully connected deep neural network with 3 hidden layers for predicting steering angles. Loss function used here is Mean Squared Error.

Prerequisites
Python has been used as the primary programming language and PyTorch as the Deep Learning framework. Other resources / software / library could be found as follows.

Self-driving car simulator developed by Udacity with Unity. Download here

Install PyTorch environment (latest version the best) in your local machine.

Log in Google Colab (if you do not have GPU and would love to utilize the power of GPU, please try this and be sure to enable GPU as accelerator)

Usage
python3 drive.py model/model.pth  
Dataset
The Udacity provided dataset works well but it is not enough to get the car running in difficult terrain (like the second track in Udacity simulator). To gather the data from track 2, at first a folder is needed to be created in the project directory. Let’s call this folder "data". Now, start the simulator. Select the second track from the menu and go to the training mode option.

Menu

Click "RECORD" button on the right corner and select a directory as the folder to save your training image and driving log information.

Record

SelectDir

Click "RECORD" again and move your car slowly and carefully. After you have completed recording your move, the training data will be stored in the folder you selected. Here record at least 3 laps of the race. Please try best to stay at the center of the road. Also, record laps in reverse direction as it will give more data and thus would help avoid overfitting.

Data
Left	Center	Right
		
/IMG/ - recorded images from cneter, left and right cameras.
driving_log.csv - saved the image information and associated information like steer angle, current speed, throttle and brake.
Training Network
Below fig shows architecture used in the project.

Network

Results
Training loss vs Validation loss

Training loss vs Validation loss (generalized)

Demo
Watch the video
