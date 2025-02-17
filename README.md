# Hack-2-Detect

This repository contains the code and documentation for our multi-camera person detection, tracking, and re-identification pipeline. Our objective is to process video data from multiple cameras to detect individuals, track their movements, re-identify them across different views, and generate final highlighted videos along with detailed reports of each person's last seen location.

---

## Team Information

- **Team Name:** Team=Lzzy
- **Team Leader:** Kushal Patel
- **Team Members:** Kushal Patel, Nirmal Patel, Jatan Patel, Jaydeep Solanki

---

## Project Overview

Our pipeline is organized into the following main modules:

1. **Data Acquisition & Preprocessing**  
   - Sourced from the "Large Scale Multi-Camera Pedestrian Detection Dataset" on Kaggle.
   - Reduced the dataset to 3 cameras with 2-3 minute segments.
   - Extracted and organized video frames by camera for further processing.

2. **Person Detection & Tracking**  
   - Utilized a state-of-the-art YOLO-based model to detect persons in every frame.
   - Applied filtering to remove low-confidence detections.
   - Implemented DeepSORT to track detected persons across frames within each video.

3. **Re-Identification & Video Combination**  
   - Extracted feature vectors for each individual using a CNN-based re-ID model.
   - Merged temporary track IDs into unique global IDs across different cameras.
   - Combined video segments from multiple cameras to generate a comprehensive highlight video for each person.

4. **Output Generation**  
   - Produced final highlighted videos with overlaid bounding boxes and global IDs.
   - Generated a report detailing the last known location of each individual (camera and timestamp).

---

## Pipeline Diagram

Below is our pipeline diagram that visually represents the entire process:

![Pipeline Diagram](https://github.com/kushalpatel0265/Person-Re-identification-through-multiple-camera/blob/main/Pipeline.png)
