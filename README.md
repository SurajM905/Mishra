# Deep_learning_project
Authors - Manish Mishra, Prerna Singh, Mohammed Danish, Anjani Josyula
This repository consists of details of course project for CMU-11785. The authors worked on 'Neural Style Transfer' during the course of Spring 2021. This repository consists of details about the experiments and results performed by the authors.

Aim of the project: Given a content image and style image, the network produces an image which looks like content image "painted" like the style image.


## Baseline Implementation
We implemented the state-of-art paper 'A Neural Algorithm of Artistic Style' by Leon A. Gatys et al. The code for the same is available in '' file.
This code was open source. We modified it to run on different contant and style images. 

## Experiments
We performed the following experiments during the course of the semester:
1) Implemented the baseline approach using content and style images and took a stylized output of the content images. 
2) We extended the idea of neural style transfer to videos, using inference on a frame-by-frame basis. 
3) In addition, we tried a pre-processing techniques - histogram matching.
4) We also tried a technique in which the previous styled output was used as the starting point for the next frame’s iteration. 

### Neural Style Transfer to Videos
In this part, we extended the baseline to videos. We performed inference for every frame in the video. To know more about the experiments, run the 'video_Neural_Style_Transfer_with_Eager_Execution.ipynb'.

### Pre-Processing for Videos - Histogram Matching
This was done using histogram matching since luminance style transfer didn't produce good results in the single frame outputs taken before midterm. This was performed by transforming the style image to reflect each content frame' color histogram before applying inference. By performing this operation for every frame, we ensured that there was a smoothness of color representation between frames - without distortion. The output was much better in terms of being representative of the actual content images' colors.
