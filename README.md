# Car-license-plate-recognition

This Notebook is about license plate recognition using python open cv to manipulate the image and  library and pytesseract to extract the text from the image.

## Requirements
 For this project we need to use: 
 
 ### Programming Language
 
 * Python 3 ~ to write the codes in simple and english like way
 
 ### Environment 
 
 * Anaconda or miniconda or google colab  ~ for package management. but it can also work on sypyder or pyzo
 
 ### Libraries
 
 * Numpy ~ for mathematical computation such as fast fourier transform to manipulate the image in frequency domain.
 * Matplotlib ~ for drawing the graphs and the processed images in different cycles
 * python-open-cv library(cv2) ~ for image manipulation and processing 
 * pytesseract ~ to extract the text from the final processed image
 
 ### Input image
  
  I have used  the following  cropped image of a car license plate as an input to be processed.
  

 <img src='https://github.com/tewodrosseble/Car-license-plate-recognition/blob/main/license.jpg' width=450>
 
 
 ### The Process work flow 
 
 After importing the image it will be changed into black and white using open cv gray scaling functions. The gray scaled picture will then be transformed into *Gaussian Blur* which is used to blurr the image using Gaussian functions to smoothen or remove unwanted  image noise and reduce the detail.
 
 Random contours will be drawn on the gaussian blurred image in order to make smooth shape on the image and create a closed region. We will chunck closer contours to simplify the analysis. 
 
 After contouring the image we need to change the image into frequency domain using *FAST FOURIER TRANSFORM * algorithm using numpy fft function. 
 
 
 <img src='https://github.com/tewodrosseble/Car-license-plate-recognition/blob/main/frequency.png' width=450>
 
 In the frequency doman we can reduce low frequency components using *high pass filter* which is a filter that passes signals with a frequency above the cutoff frequency and attenuates those below the cutoff frequency. This will reduce unnecessary parts with low frequency components on the image.
 
 
 After filtering the image using *high pass filter* we will compute the inverse fast fourier transform of the image to continue the analysis.
 
 By drawing rectangular planes on the concentrated contours we can create a rectangular group of contours which will then be reduced to give a cropped picture of the license number as follows.
 
 <img src='https://github.com/tewodrosseble/Car-license-plate-recognition/blob/main/final_extracted.png' width=450>
 
 ## Application Areas of License plate recognition system
 This project can be used in 
 
 * Police and Law Enforcement 
 * Autorization and Authentication
 * Security systems
 * Inventory 
 * Traffic Control 
 * Tolling and Smart Billing
 * Ticket less parking 
 * Stolen vehicle detection ....
 
 ## Scalabilty of the project
 
 This project can be scaled upto 
 
 * Real time video survilance based vehicle number identification 
 * Web based license number database system
 * Criminal vehicles Information Identification
 
 
 Tewodros Seble  <br>
 @ All Rights Reserved
 
