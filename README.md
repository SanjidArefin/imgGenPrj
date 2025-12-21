# Project imgGenPrj
This project develops a framework for generating consistent video frames using a hybrid system. An image generator generates a single frame using pre-trained model. The system iteratively improves frame quality using similarity metrics like SSIM, ensuring semantic alignment and visual coherence. The algorithm is extracted to interpolate rest of the frame. This process combines accuracy of an image generator with efficiency of algorithm based frame generation

# Aim of this project
 1.This project aims to create a video interpolator especially for 3D & 2D animators.
 
 2.This project aims to achieve much more efficient and cheaper results by using a hybrid technique.

# Achivements
1. Achieved 45% lower cost and 26% lower resource consumption with improved consistency across frames.
2. Utilized algorithm extraction for frame generation and the SSIM loop for video-specific optimization.

# Future Work
Interface Development: Creating a user friendly interface can make commercial use of this software possible.

# To do
1. go to rife/train_log

2. upload flownet.pkl, IFNet_HDv3 RIFE_HDv3 to arXIv2020/train_log

3. upload  "your_video.mp4"  to arXIv2020

4. go to arXIv2020/inference_video.py

5. edit line-> 123 to 124

6. swap with 123 to 124 line->

   
    import imageio.v3 as iio
    
    videogen = iio.imiter(args.video)
    lastframe = next(videogen)
