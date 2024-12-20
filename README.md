# Ceiling Security Camera: Person Detection and Tracking

This project leverages **YOLOv7** for real-time object detection and **SORT (Simple Online Realtime Tracking)** for tracking individuals under a ceiling-mounted security camera. The system is optimized to detect and track people in crowded environments, offering accurate and efficient performance.

## Features
- **Real-time detection**: Utilizes YOLOv7 for precise person recognition.
- **Reliable tracking**: Implements SORT to track individuals across frames efficiently.
- **Ceiling-mounted perspective**: Optimized for overhead camera views, reducing occlusion and perspective challenges.
- **Lightweight and efficient**: Designed for high performance on modern GPUs and capable CPUs.

## Use Cases
- Monitoring public spaces such as shopping malls, airports, or event venues.
- Enhancing security systems with advanced detection and tracking capabilities.
- Data collection for crowd management and flow analysis.

## Installation

### Prerequisites
1. Python 3.8+
2. NVIDIA GPU with CUDA support (for optimal performance)
3. Required Python libraries (listed below)

### Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repo-name.git
   cd your-repo-name
   ```

2. **Install dependencies**:
   Use the following command to install required libraries:
   ```bash
   pip install -r requirements.txt
   ```
   *(Ensure the file includes dependencies like `torch`, `opencv-python`, `numpy`, and `matplotlib`.)*

3. **Run the system**:
   To start detection and tracking:
   ```bash
   python main.py --source video.mp4 --output output_folder --device 0
   ```

   Replace `video.mp4` with the input video path. Use `0` for live camera feed.


## Usage
- **Input source**: Supports live camera feeds or pre-recorded videos.
- **Output**: Generates annotated videos with bounding boxes and unique IDs for tracked individuals.

### Command-line Arguments
| Argument         | Description                                     |
|------------------|-------------------------------------------------|
| `--source`       | Path to input video or `0` for webcam.          |
| `--output`       | Path to save output video.                      |
| `--device`       | Device to run on (`cpu` or GPU ID, e.g., `0`).  |



## Acknowledgments
- **YOLOv7**: [GitHub Repository](https://github.com/WongKinYiu/yolov7)
- **SORT**: [Original Paper](https://arxiv.org/abs/1602.00763)

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
