# Stauffer-Grimson-Adaptive-Background-Mixture-Model

## Submitted By:
- Abhilash 
  
## “Background Subtraction Using Gaussian Mixture Model”

### Introduction
In this project, our main goal was to use Gaussian Mixture Models (GMM) to make videos more interesting by removing the background and highlighting the movement happening in the foreground. We did some experiments to adjust different settings of our model and see how it affected the background subtraction we were using. It's like finding the perfect recipe for making the foreground stand out in videos.

### Methods
1. **Initialization**:
   - Open the video file and read the first frame.
   - Convert the frame to grayscale and extract its dimensions.

2. **Video Writers Initialization**:
   - Initialize video writers for saving the background and foreground frames.

3. **Parameter Initialization**:
   - Initialize parameters such as threshold, learning rate, second learning rate, and the number of frames.

4. **Gaussian Distribution Initialization**:
   - Initialize mean, variance, and weight for each pixel assuming three Gaussian distributions.

5. **Main Processing Loop**:
   - Iterate through each frame of the video.
   - For each pixel, update the Gaussian distribution parameters based on the current frame.
   - Classify each pixel as background or foreground based on the learned distributions and threshold.
   - Save the background and foreground frames as images.
   - Repeat until all frames are processed or the user interrupts the loop.

### Inferences
**Hyperparameters**:
- Learning Rate (α)
- Background Ratio (T) is a measure of the minimum portion of the data that should be accounted for by the background.

| Learning Rate (α) | Background Ratio (T) | Conclusion |
| ----------------- | -------------------- | ---------- |
| 0.01              | 0.5                  | Model is Converging Slowly so Noise is less |
| 0.1               | 0.5                  | Model is Converging Rapidly so Noise is more |

#### Visuals
- α = 0.01, T = 0.5
- α = 0.1, T = 0.5

### References
- Stauffer, C., and Grimson, W. 1999. Adaptive background mixture models for real-time tracking. In Computer Vision and Pattern Recognition.
- P. Wayne Power, Johann A. Schoonees, 2002. Understanding Background Mixture Models for Foreground Segmentation. Proceedings Image and Vision Computing New Zealand, University of Auckland, Auckland, New Zealand.
