# Digital-image-processing
BRAIN TUMOR DETECTION USING IMAGE PROCESSING
ABSTRACT

Brain tumor detection is the most difficult and tedious task in medical imaging. Magnetic resonance imaging (MRI) can be a medical procedure that is generally used by the medical specialist to show the internal structure of the structure without surgery. Magnetic resonance imaging provides a lot of information about sensitive human tissue, which helps infer brain tumors. Accurate segmentation of the 
MRI image is critical for concluding a brain tumor with a laptop-compatible clinical device. This report focuses on the best and most correct approach to detecting neoplasms by brain MRI and, if it confirms the presence of a tumor, focuses on evaluating its stage. We conducted an experiment. Showed that our proposed methodology offers greater precision than the various existing strategies for tumor detection.

INTRODUCTION

This project proposes to segment a tumor from a magnetic resonance image and identify the tumor. For this purpose, segmentation and grouping techniques were implemented. Each MRI image is passed through an image chain where the image is pre-processed to remove noise and improve image contrast. The application of each of the segmentation techniques allows us to determine the most appropriate method of segmenting the tumor for each of the images. In this project, the most important challenge was to locate and extract the correct tumor region from the image. Due to various lighting issues, there were unnecessary white areas in the image that could be incorrectly segmented as a tumor. In addition, unwanted noise and reduced contrast reveal several areas of the image that are incorrectly labeled as a tumor. Another challenge was the degraded quality of the MRI image due to various issues that would have arisen during the acquisition phase.
PROPOSED METHOD

In this project we have described our goal as brain tumor detection, ie the presence of the tumor on the provided MRI. Here we will analyze the MRI images that conclude the stage of the tumor. In general, the diagram for our process. The input images go through several stages that can be summarized as shown in Figure 1.


MRI of Brain Images
 
Pre-Processing
 
Feature Extraction
 
Segmentation Technique
 
Image Analysis
MRI of Brain images

This is the first step of our proposed project .In this the data has been provided that is the magnetic resonance images(MRI) that are been collected in their original format’s that are (.ima, .dcm). Mostly the mri images are of .dcm (DICOM[13]) Digital imaging and communications in medicine. We have used file operations fopen(), fclose() available in matlab to read MRI images. Here the gray scale MRI images are being provided as input to the system.

Pre-Processing

Pre-processing phase of our project mainly involves those operations that are ordinarily essential before the goal analysis and extraction of the required data and ordinarily geometric corrections of the initial image. These enhancements embrace correcting the information for irregularities and unwanted region noise, removal of non-brain element image and converting the data so that they are correctly reflected in the original image. The first step of pre- processing is the conversion of the given input MRI image into a suitable form on which further work can be  performed.
This conversion of DICOM image to .jpeg is done by using function dicom2image()[7]. Major issues related to the pre- processing stage are as follows:-
•	Noise,
•	Blur Low Contrast,
•	The partial-volume effect.
This pre-processing stage is used for reducing image noise, highlighting important portions, or displaying obvious portions of digital images.

De-noising method

Despite the presence of considerable variety of state-of-the-art ways of de-noising however correct removal of noise from magnetic resonance imaging image is a challenge. Here, Filter based method has been used as a de-noising. We have used the Filter transform functions that is anisotropic diffusion. By the help of these functions noise has been removed from the taken input that is the MRI image. These functions make it possible to recover weak signals from noise and the processed image in this way can be cleaned up without blurring or losing the clarity.
Images Enhancement and Filtering
In this project image improvement that is the improvement of digital image quality with none of the data concerning the first supply image degradation. The enhancement of the image starts by first converting the gray scale image to black and white image this is done using function im2bw(gray_image)[7].Here the threshold value taken in our project is 0.6.As Image improvement strategies improve the visual look of pictures from tomography and the distinction enhancing brain volumes are linearly associated. For image sharpening the imsharpen () [7] has been used, similarly imadjust () [7] for image adjustment, freqz () for setting frequency response of image are being used. The Gaussian smoothing operator has been for the two-dimensional image convolution operators that is used to `blur' images and remove detail and noise. Gaussian is random incidence of white intensity worth, and its intensity worth is drawn from Gaussian distribution, thus it is very much use to reduce Gaussian noise and as with linear filter it is computationally economical and enhances image quality with the image boundaries for implementation of Gaussian filter the imgaussfilt()[7] has been used in our project. Color areas, which indicate the colors in an exceedingly benchmark approach by employing a reference frame and a topological space within which every color is delineated by one point of the coordinate system. The color spaces used in our image processing methods are Gray, Binary form and RGB.

Feature Extraction
In this phase the features of the given input image have been extracted. These features include smoothness, entropy, variance, kutosis, skewness, idm, correlation, homogeneity, mean and standard deviation . And based on these features the image is analyzed and the detection of the tumor region has been done. Below in the figure 2 there are output result of an mri image until the feature extraction phase of the project.

Thresholding

Thresholding is a type of image segmentation, where we change the pixels of an image to make the image easier to analyze. In thresholding, we convert an image from colour or grayscale into a binary image, i.e., one that is simply black and white.

Morphological Operation

Morphology is a broad set of image processing operations that process images based on shapes. Morphological operations apply a structuring element to an input image, creating an output image of the same size.

