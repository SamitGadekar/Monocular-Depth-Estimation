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

# Features

- Converts single images into depth maps using the DepthAnything implementation via HuggingFace.
- Stitches images and depth maps into a point cloud using basic camera intrinsics assumptions.


# Custom Modifications

- Compatible with Mac (MPS) and can default to CPU when needed.
- Matplotlib visualizer runs outside of enclosed IDEs for more accurate and standardized display.
- Visualizes point clouds via Open3D’s native visualizer.
- Includes a GUI for real-time modification of camera intrinsics and other parameters to fine-tune point clouds for improved accuracy.


# Possible Future Additions

- Scale the output to metric units by utilizing the MetricDepth model on HuggingFace (loading checkpoints into PyTorch for custom inference).
