# YouTube Object Detection with YOLOv8 (Bird & Drone Focus)  

This project leverages the power of YOLOv8 (You Only Look Once v8) for real-time object detection in YouTube videos, with a specific focus on identifying birds and drones.

[![Drone and Bird Detection](object_detection_videos/object_detection_videos.mp4)]
[![Drone and Bird Detection](object_detection_videos/object_detection_videos.mp4)](object_detection_videos/object_detection_videos.mp4)

## Functionality Overview

- **Imports necessary libraries:** OpenCV (cv2), ultralytics (for YOLOv8) , math (for potential calculations ), and pytube (for YouTube video handling ).
- **Loads the pre-trained YOLOv8 model:** You'll need to replace the path (`'C:/Users/user/Data_Ana_3/Final_files/runs/detect/yolov8sdronebirdlight.pt/weights/best.pt'`) with the location of your trained model weights file specifically optimized for bird and drone detection (70 times training ).
- **Defines YOLOv8 classes:** This list likely contains the object classes your model can recognize (e.g., "bird", "drone", etc.) .
- **Fetches YouTube video URL (replace with your desired video ):** You can paste the URL of a YouTube video you want to analyze here. Consider providing multiple example URLs in the comments section for users to experiment with  .
- **Extracts video stream URL:** pytube is used to obtain a downloadable video stream URL from the provided YouTube video URL 🪄.
- **Configures webcam with the video stream URL:** This is a creative touch, allowing users to analyze the video using their webcam as if it were a live feed . Note that this functionality might require further adjustments depending on your use case .
- **Enters a continuous loop:**
    - Captures a frame from the "webcam" (referencing the video stream URL).
    - Checks if the frame is valid (not None).
    - Performs YOLOv8 object detection on the frame using the loaded model.
    - Iterates through detection results:
        - Draws bounding boxes around detected objects with a confidence score above 0.5 (you can adjust this threshold).
        - Displays the object class name and confidence score near the bounding box.
- **Displays the processed video frames:** Presents the video with detected objects highlighted  ✨.
- **Waits for user input:** Exits the loop when the 'q' key is pressed .
- **Releases resources:** Properly releases the "webcam" capture and closes all windows .

## Usage Instructions

1. **Install required libraries:** Make sure you have OpenCV (cv2), ultralytics, math, and pytube installed. You can use `pip install opencv-python ultralytics pytube` in your terminal .
2. **Replace the YOLOv8 model path:** Update the path in the code to point to your trained YOLOv8 model weights file. This model should be specifically trained for bird and drone detection .
3. **Replace the YouTube video URL (optional):** If you don't want to use the webcam functionality, uncomment the `video_url` line and paste the URL of the YouTube video you want to analyze  ➡️ [link to YouTube video](https://www.youtube.com/).
4. **Run the script:** Execute the Python script (e.g., `python object_detection.py`) .

## See the Demo Video

**Option 1: Direct Link (if video is small and for limited audience):**

You can download the demo video by clicking the link below:

[Watch the Demo Video](object_detection_videos/object_detection_videos.mp4) ️

**Option 2: Using a Video Hosting Platform (recommended):**

Here's a demo of the object detection in action:

<iframe width="560" height="315" src="VIDEO_URL" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen></iframe>

**Replace `VIDEO_URL` with the actual URL of your video player provided by the hosting platform (e.g., YouTube, Vimeo).**

## Potential Enhancements

- Consider adding support for multiple video formats beyond MP4 .
- Provide options to adjust the confidence threshold for bounding box display ️.
- Explore integrating distance estimation or other calculations based on object detection results .
- Allow users to specify a region of interest (ROI) within the frame for focused detection .
- Implement a user interface for more interactive control  ️.

## Contributing

We welcome contributions to this project! Feel free to fork the repository, make your changes, and submit a pull request .

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
