
# People Tracking with YOLOv8 and Custom ID Assignment

This project demonstrates real-time people tracking in videos using the YOLOv8 object detection model, with a custom lightweight tracking logic for assigning stable person IDs and visualizing their motion paths.

##  Example Output

<!-- Uploading "cv_img.jpeg"... -->

---

## Features

- Person detection using YOLOv8x
- ID assignment for tracking people
- Path tracking using Euclidean distance
- Visual overlays for bounding boxes, IDs, and paths
- Supports any `.mp4` video input

---

## Installation

Run the following commands to set up the environment:

```bash
pip install -q ultralytics
pip install -q deep_sort_realtime
```

##  Usage

1. Place your input video in the project directory and rename it `input.mp4`.
2. Run the Python script. It will generate an annotated output video named `output_video.mp4`.


---

##  How It Works

- **Detection**: Uses YOLOv8 to detect persons in each frame.
- **Tracking**: Assigns IDs based on proximity using Euclidean distance.
- **Visualization**: Draws bounding boxes and trails for each person in distinct colors.

---

##  Project Structure

```
├── track_people.py         # Main script
├── input.mp4               # Input video (add manually)
├── output_video.mp4        # Generated output
```

---

##  Sample Results

- Accuracy: people pathes detected without overlapping 
- FPS: Depends on hardware (YOLOv8x is heavier than other models)

---

##  License

MIT License

