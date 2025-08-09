# Overview

Monocular-Depth-Estimation leverages state-of-the-art depth estimation models to convert 2D images into detailed depth maps, which are then transformed into 3D point clouds. Using basic camera intrinsics assumptions, it enables visualization and interactive exploration of these point clouds via Open3D and matplotlib. Additionally, the project features a user-friendly GUI for real-time tuning of camera parameters like field of view (FOV) and depth scaling, allowing fine control over the generated 3D representations.

Ideal for researchers and developers working in computer vision, robotics, or 3D reconstruction, this tool provides a foundation for advanced depth sensing and visualization workflows!


# Inspiration

This project is inspired by the live course [2D Image to 3D Point Cloud with DepthAnything: Live Course (Monocular Depth Estimation)](https://www.youtube.com/watch?v=2Jl-ZeQJzwI) by Florent Poux, which utilizes the [Depth-Anything](https://github.com/LiheYoung/Depth-Anything) model. The video walkthrough demonstrates how to convert single 2D images into depth maps and reconstruct 3D point clouds using state-of-the-art depth estimation techniques. Building on this foundation, I have implemented additional features such as real-time GUI controls for camera intrinsics and extended compatibility for Mac systems to enhance usability and flexibility.


# Features

- Converts single images into depth maps using the Depth-Anything implementation via HuggingFace.
- Stitches images and depth maps into a point cloud using basic camera intrinsics assumptions.


# Custom Modifications

- Compatible with Nvidia GPUs (CUDA), Mac (MPS), and can default to CPU when needed.
- `Matplotlib` visualizer runs outside of enclosed IDEs for more accurate and standardized display.
- Visualizes point clouds via `Open3D`’s native visualizer.
- Includes a GUI for real-time modification of camera intrinsics and other parameters to fine-tune point clouds for improved accuracy.


# Requirements

Make sure to install and have the following packages available:

- `numpy`
- `torch`
- `transformers` (for `AutoImageProcessor` and `AutoModelForDepthEstimation`)
- `opencv-python` (`cv2`)
- `matplotlib` (use `'TkAgg'` backend to avoid PyCharm color grading effects)
- `open3d`
- `os`, `random`, `pathlib` (standard libraries)

Optional, for advanced visualization application:
- `tkinter`, `ttk` (from `tkinter`)


# Possible Future Additions

- Scale the output to metric units by utilizing the MetricDepth model on `HuggingFace` (loading checkpoints into `PyTorch` for custom inference).
- Object/environment recognition within point clouds.
- ROS implementation for real-time depth estimations and visualizations based on live-video feeds.
- LiDAR comparison convergences to estimate accurate camera intrinsics and Depth-Anything parameters.


## Contributing

If you'd like to contribute, feel free to submit issues or pull requests to enhance this project further!
