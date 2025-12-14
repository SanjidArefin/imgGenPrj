# imgGenPrj

Developed an image-to-video generator, which uses a pre-trained model with SSIM-guided video-specific refinement to produce an “action frame” from which it  extracts the algorithm to populate the remaining frame.


1. Achieved 45% lower cost and 26% lower resource consumption with improved consistency across frames 
2. Utilized algorithm extraction for frame generation and the SSIM loop for video-specific optimization

# To do

1. From GitHub rife-> CLI usage ->Download the pretrained HD models from here.

2. upload->rife->train_log->flownet.pkl+IFNet_HDv3+RIFE_HDv3

3. upload -> "your_video.mp4" ->arXIv2020

4. go to->arXIv2020->inference_video.py

5. edit line-> 123 to 127

6. swap with 123 to 126 line-> 
    import imageio.v3 as iio
    
    videogen = iio.imiter(args.video)
    lastframe = next(videogen)
