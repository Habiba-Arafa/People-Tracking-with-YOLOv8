
# People Tracking with YOLOv8 and Custom ID Assignment

This project demonstrates real-time people tracking in videos using the [YOLOv8](https://github.com/ultralytics/ultralytics) object detection model, with a custom lightweight tracking logic for assigning stable person IDs and visualizing their motion paths.

## 📸 Example Output

![Sample Output](f3fd806c-1687-4c23-aa8c-bb793ff0101a.png)

---

## 🎯 Features

- Person detection using YOLOv8x
- Custom ID assignment for tracking up to 3 people
- Path tracking using Euclidean distance
- Visual overlays for bounding boxes, IDs, and paths
- Supports any `.mp4` video input

---

## 🔧 Installation

Run the following commands to set up the environment:

```bash
pip install -q ultralytics
pip install -q deep_sort_realtime
```

> The current implementation uses only YOLO and custom logic (Deep SORT installed but not used).

---

## ▶️ Usage

1. Place your input video in the project directory and rename it `input.mp4`.
2. Run the Python script. It will generate an annotated output video named `output_video.mp4`.

```python
# Replace with your input/output paths
input_video_path = '/content/input.mp4'
output_video_path = 'output_video.mp4'
```

---

## 🧠 How It Works

- **Detection**: Uses YOLOv8 to detect persons in each frame.
- **Tracking**: Assigns IDs based on proximity using Euclidean distance.
- **Visualization**: Draws bounding boxes and trails for each person in distinct colors.

---

## 📁 Project Structure

```
├── track_people.py         # Main script
├── input.mp4               # Input video (add manually)
├── output_video.mp4        # Generated output
├── f3fd806c...01a.png      # Example screenshot
└── README.md               # Project documentation
```

---

## ✅ Sample Results

- Accuracy: Good for up to 3 people with stable motion
- FPS: Depends on hardware (YOLOv8x is heavier than other models)

---

## 📌 Notes

- You can replace YOLOv8x with smaller versions (like `yolov8n.pt`) for faster performance.
- The `deep_sort_realtime` package is optional and can be used for more robust multi-object tracking if needed.

---

## 📃 License

MIT License

---

## 👤 Author

Habiba Muhammed  
Zewail City of Science & Technology  
Course: DSAI 305 - Interpretability & Explainability in AI
