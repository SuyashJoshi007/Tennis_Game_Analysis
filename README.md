Advanced Tennis Analysis with Computer Vision 🎾

This project leverages state-of-the-art computer vision techniques to perform in-depth analysis of tennis match videos. It automatically detects and tracks players and the ball to calculate key performance metrics like player speed, ball speed, and total shots played.

This repository is an excellent hands-on project for anyone looking to apply and polish their skills in object detection, model fine-tuning, and overall machine learning engineering.

🎥 Project Demo

Here is a screenshot from a sample output video, where players are tracked, and metrics are displayed in real-time.

A snapshot of the real-time player and ball tracking with on-screen analytics.

✨ Key Features

🏃‍♂️ Player Tracking & Speed Measurement: Detects both players on the court and calculates their movement speed in real-time.

☄️ Ball Tracking & Shot Speed Calculation: A fine-tuned YOLO model accurately tracks the tennis ball to measure shot speeds.

📊 Automated Shot Counter: Automatically counts the number of shots played by each player during a rally.

🔑 Court Keypoint Detection: A custom CNN model identifies key points of the tennis court to provide spatial awareness and context for the analysis.

⚙️ How It Works & Models Used

The analysis pipeline is built on a foundation of powerful deep learning models:

Player Detection: YOLOv8 is used for robust, real-time detection of players on the court.

Ball Detection: A fine-tuned YOLOv5 model is used specifically for the challenging task of detecting a small, fast-moving tennis ball with high accuracy.

Court Geometry: A custom PyTorch CNN extracts key points of the court (e.g., corners, service lines), which is crucial for perspective transformation and accurate metric calculation.

Pre-trained Models

The custom-trained models are available for download:

YOLOv5 Tennis Ball Detector: Download from Google Drive

Tennis Court Keypoint Model: Download from Google Drive

🚀 Getting Started

Follow these instructions to set up and run the project on your local machine.

Prerequisites

Python 3.8 or newer

pip and venv for package management

Installation

Clone the repository:

git clone [https://github.com/your-username/tennis-analysis.git](https://github.com/your-username/tennis-analysis.git)
cd tennis-analysis


Create and activate a virtual environment:

python3 -m venv venv
source venv/bin/activate
# On Windows, use: venv\Scripts\activate


Install the required dependencies:
Create a requirements.txt file with the content below and run pip install -r requirements.txt.

ultralytics
torch
torchvision
pandas
numpy
opencv-python


pip install -r requirements.txt


Download the pre-trained models:

Download the models from the links provided above.

Create a models/ directory in the root of the project.

Place the downloaded model files (.pt or .pth) inside the models/ directory.

Usage

To run the analysis on a video file, execute the main script from the command line:

python main.py --video_path "path/to/your/tennis_video.mp4"


The script will process the video and save the output with the analysis overlay in the output_videos/ directory.

🧠 Model Training

The Jupyter notebooks used for training the custom models are available in the training/ directory. You can use these to understand the training process or to retrain the models on your own custom datasets.

Tennis Ball Detector (YOLOv5): training/tennis_ball_detector_training.ipynb

Court Keypoint Extractor (PyTorch): training/tennis_court_keypoints_training.ipynb

📄 License

This project is licensed under the MIT License. See the LICENSE file for details.
