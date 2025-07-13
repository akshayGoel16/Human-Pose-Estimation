# Human Pose Estimation - *PoseSnapper*

This project demonstrates **real-time human pose estimation** on images using **OpenCV's DNN module** and a pre-trained TensorFlow model. The app is built with **Streamlit** to provide an interactive web interface where users can upload images and view detected body keypoints and connections.

---

## Features

- Upload your own image or use the default demo image
- Detects key human body parts like elbows, wrists, knees, shoulders, etc.
- Draws pose skeletons using pre-defined body part connections
- Adjustable **threshold slider** to fine-tune keypoint detection
- Lightweight and fast — runs directly in your browser using Streamlit

---

## How It Works

- Loads a **pre-trained TensorFlow model** (`graph_opt.pb`) for human pose detection
- Converts the input image into a blob using OpenCV's `cv2.dnn.blobFromImage`
- Performs forward pass through the DNN to get confidence heatmaps
- Maps the most confident keypoints and connects them using **POSE_PAIRS**
- Visualizes the output with **ellipses** and **lines** connecting joints

---

## Tech Stack

- **Python 3**
- **OpenCV (cv2.dnn)**
- **Streamlit** for the web interface
- **NumPy**, **Pillow (PIL)** for image handling

---

### ▶️ To run the app:

```bash
pip install -r requirements.txt
streamlit run your_script_name.py (Ex: pose_estimation.py)
