# Multi-Person Pose Tracking with YOLOv8 and Mediapipe

This project combines **YOLOv8** for object detection and **Mediapipe Pose** for pose estimation to track and visualize human body poses in real-time or from video files. It supports GPU acceleration using TensorFlow for enhanced performance.

## Features
- **Multi-Person Detection and Pose Tracking:** Detect multiple objects and estimate poses within detected bounding boxes.
- **YOLOv8 Integration:** Utilizes YOLOv8 for robust and accurate object detection.
- **Pose Visualization:** Visualize human body pose landmarks with dynamic rainbow-colored connections.
- **GPU Acceleration:** TensorFlow is used to enable GPU memory growth for efficient processing.

## Requirements
Before running the project, ensure the following are installed:

- Python 3.8 or higher
- Required libraries:
  ```bash
  pip install opencv-python mediapipe numpy tensorflow ultralytics
- A CUDA-compatible GPU (optional but recommended for faster inference).

## Usage
1. Clone the Repository:
   ```bash
   git clone https://github.com/yourusername/multi-person-pose-tracking.git
   cd multi-person-pose-tracking
  
2. Download the YOLOv8 model weights:
    - You can use the pre-trained YOLOv8 nano model (yolov8n.pt).
      
3. Place your video file in the project folder, or replace the path in the code or `0` to use Webcam:
   ```bash
     cap = cv2.VideoCapture(r"path/to/your/video.mp4") || cap = cv2.VideoCapture(0)                            

4. Run the script:
   ```bash
   python pose_tracking.py
5. The following windows will appear:
    - Multi-Person Pose Tracking: Displays the input frame with bounding boxes and pose connections.
    - Pose Only (Landmark and Connections): Displays the detected poses on a blank image.

6. Press the `x` key to exit the program.

### Project Structure
-  ```bash
   multi-person-pose-tracking/
      ├── pose_tracking.py       # Main script for pose tracking
      ├── LICENSE                # Project license
      └── README.md              # Project documentation

## Results
- Human poses are detected and visualized within the bounding boxes identified by YOLOv8.
- Each pose connection is dynamically assigned a color from a predefined rainbow color palette.

## Acknowledgments
- YOLOv8 (Ultralytics): For object detection and bounding box identification.
- Mediapipe Pose: For human pose estimation and landmark detection.
- OpenCV: For video capture, processing, and visualization.
- TensorFlow: For enabling GPU memory growth and optimizing performance.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
