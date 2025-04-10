# Setup Instructions for SoccerNet Football AI Project

This document provides step-by-step setup guidance for running the full SoccerNet-based AI pipeline locally. This includes installing dependencies, configuring paths, and launching the pipeline for inference or development.

---

## 1. Requirements

Ensure you have the following installed:

- Python 3.9 or newer
- Git
- FFmpeg
- pip
- virtualenv (optional but recommended)
- CUDA/cuDNN (for GPU acceleration, if applicable)

---

## 2. Clone the GitHub Repository

```bash
git clone https://github.com/bndo01/ABBW.git
cd ABBW
```

---

## 3. Set Up Python Environment

It's highly recommended to use a virtual environment:

```bash
python -m venv venv
venv\Scripts\activate  # Windows
# OR
source venv/bin/activate  # macOS/Linux
```

---

## 4. Install Dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

## 5. Model Files and Videos

The full set of models and videos are not hosted on GitHub due to size.  
Download them from Google Drive:

**Google Drive:**  
[Download Full Project Files](https://drive.google.com/file/d/1S-tYcSvdcfSM79XOodPtoaZrg0iUYVMZ/view?usp=sharing)

After downloading:
- Place the model weights in the `models/` directory.
- Place video input files in `input/` or as configured.

---

## 6. Running the Unified Pipeline

To begin real-time inference and event detection:

```bash
python unified_pipeline.py
```

This script:
- Runs YOLOv11x-seg for player and ball detection.
- Applies DeepLabv3 for field zone segmentation.
- Extracts features from video clips.
- Detects events using the SoccerNet spotting module.
- Generates CSV logs and annotated video output.

---

## 7. Output Files

Output files will be saved to:

- `output/` — includes features, clips, predictions
- `event_files/` — event detection logs
- `annotated_video.mp4` — final output video with overlays

---

## 8. Live Stream Processing (Optional)

To process a live stream (e.g., from an IP camera or local server), update the source in `unified_pipeline.py`:

```python
VIDEO_SOURCE = "http://your-stream-url/stream.m3u8"
```

Then run the pipeline again.

---

## 9. Real-Time Web Display (Optional)

To enable real-time AR overlays on a webpage:

1. Start the WebSocket server:

```bash
python ws_server.py
```

2. Open `index.html` in your browser to view the video with event overlay updates.

---

## 10. Support

For any issues, please reach me out +966500191104 Email ,alanazi1.bandar@gmail.com


---

