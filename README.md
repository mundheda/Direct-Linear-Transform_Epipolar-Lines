# Direct-Linear-Transform_Epipolar-Lines
Direct linear Transform (2D-3D) from an image to given points in the 3D world. Then using Zhangs method to find K matrix of the Camera. Also Generating Epipolar Lines b/w two images with different camera positions.

## DLT and Epipolar Lines

The goal is to aid your understanding of the Direct Linear Transform as well as Epipolar geometry.

For the first part, found correspondences between 2D-3D points and estimate the P Matrix. Then estimated Camera Parameters from this P matrix.

In the second part, constructed epipolar lines on two corresponding images.

### Generating Correspondences
The first step to perform DLT is to generate correspondences. The cell below opens a new window. Clicking anywhere on the image should give you the pixel location of the image. Once you're done clicking, close the image window. The cell after displays the points you have clicked.

After generating pixel locations, you have to generate the corresponding world points. You have the freedom to chose which point you want as origin. You can consider each side as 4 units.

### Zhangs method

For this task, use the inbuilt Opencv function to estimate the K matrix of a camera. Use the checkerboard images 5456-5470 in images/zhangs folder for this task. Familiarize yourself with the different parameters for this method.

### Epipolar lines

Two images of the same scene taken from different view-points. The fundamental matrix that encodes their relative geometry as well as a subset of corresponding points have been provided to you. The images are in q2 folder.

Recall that given a point in one image, it's corresponding location in the other image can be found to along a line viz. the epipolar line. The task given to you is to draw the epipolar lines in the second image for each given point in the first image. You have to repeat this for the other image as well. Draw epipolar lines on the first image for the corresponding points in the second image.

The convention used for F is $x'^{T}Fx$ where $x'$ is the location of the point in the second image.

