# **Pose_Detection_System**

This project implements a **basic pose detection system** that detects key pose points (e.g., shoulders, hips, knees) from a video of a person performing squats. It calculates the **knee bend angle** in each frame and outputs the angle sequence along with a visualized graph.

---

## **Objective**
- Use a pre-trained **pose estimation model** like Mediapipe to detect key pose landmarks.
- Calculate the **knee bend angle** using hip, knee, and ankle points.
- Display pose landmarks and angles on the video frames.
- Output the knee angle sequence and plot it over time.

---

## **Technologies Used**
- **Python** (Google Colab)
- **Mediapipe**: Pose detection model for identifying body landmarks.
- **OpenCV**: Video processing and annotation.
- **Matplotlib**: Visualization of knee bend angle over time.
- **Numpy**: For trigonometric angle calculations.

---

## **Setup and Execution**

Follow these steps to run the project in Google Colab:

1. **Clone the Repository**:
   ```python
   git clone https://github.com/your-username/pose-detection-challenge.git
   cd pose-detection-challenge
   ```

2. **Open in Google Colab**:
   - Upload the pose_detection.ipynb notebook to Google Colab.

3. **Install Required Libraries**:
   - Run the following commands in a Colab cell:
     
    ```python
    !pip install mediapipe opencv-python-headless matplotlib
    ```
    
4. **Upload the Input Video**:
   - Use the files.upload() method in Colab to upload your video file (e.g., example_video.mp4).
  
5. **Run the Notebook**:
   - Execute all the cells in the notebook to:
  
     - Process the video.
     - Detect pose landmarks.
     - Calculate and display knee angles.
     - Plot the knee bend angle graph.

---

## **Features**

- Pose Detection:
   - Detects key body points (shoulders, hips, knees, ankles) using Mediapipe's pre-trained Pose model.

- Knee Angle Calculation:
   - Computes the knee bend angle in real time using the cosine rule for three points: hip → knee → ankle.

- Video Annotation:
   - Displays pose landmarks and knee angle on each video frame.

- Graph Visualization:
   -Plots the knee bend angle over time, showing the range of motion throughout the squats.

---
  
## **Outputs**
- Processed Video:
   - Annotated frames with detected landmarks and real-time knee angle displayed.

- Knee Bend Angle Plot:
   - A line graph showing the variation of knee angles over video frames.

---

## **Example Output**
Knee Bend Angle Visualization

---

## **How it Works**
- Pose Detection:
   - Mediapipe identifies 33 pose landmarks in each video frame.
- Angle Calculation:
   - Uses trigonometry to calculate the angle formed at the knee joint (hip-knee-ankle).
- Visualization:
   - Annotates frames and plots angles for easy analysis of knee motion.

---

## **Future Enhancements**
- Handle multiple people in a single frame.
- Save the annotated video with pose landmarks.
- Apply smoothing filters to reduce noise in angle calculations.
- Add support for real-time video streams.
