

# Hand Tracking and Feedback Web App

A real-time web application for comprehensive **hand tracking, gesture analysis, and feedback** using computer vision and machine learning. The app analyzes your hand through the webcam, overlays annotated feedback, and logs each session with in-depth reports—ideal for rehabilitation, gesture research, and progress monitoring.

## Features

- **Live Hand Tracking:**
Detects and tracks hand landmarks, joints, and gestures in real time via your webcam, powered by MediaPipe.
- **Visual \& Text Feedback:**
Annotates the video stream with overlays and provides context-aware textual feedback during exercises.
- **Measurement \& Analytics:**
Calculates wrist angles, joint metrics, thumb/finger opposition, fist clench, and more.
- **Session Logging \& Reporting:**
Saves every session, generating:
    - **Excel logs** of joint angles and metrics
    - **PDF summary reports** comparing your data with clinical normal ranges
    - **PDF trend plots** of all tracked angles and motions
- **User-Friendly Frontend:**
Intuitive interface for starting sessions, viewing logs, and downloading reports.


## Demo

1. **Launch the app:**
Visit the homepage and allow camera access.
2. **Start a session:**
Receive live video overlays and immediate feedback.
3. **End session:**
Instantly access Excel, summary PDF, and plot reports for detailed review.

## Installation

**Requirements:**

- Python 3.7+
- pip

**Install all dependencies:**

```bash
pip install -r requirements.txt
```

_Required packages include:_ Flask, OpenCV, MediaPipe, NumPy, Pandas, Matplotlib.

**Run the server:**

```bash
python app.py
```

Open your browser at [http://localhost:5000](http://localhost:5000)

## Project Structure

| File/Folder | Purpose |
| :-- | :-- |
| `app.py` | Flask backend, routes, video streaming, session logic |
| `final_code.py` | HandTracker class, core ML analytics and feedback |
| `templates/` | HTML/Jinja templates: index, live, results pages |
| `outputs/` | Auto-saved session logs, reports, and plots |
| `static/` | CSS files for page styling |

## How It Works

- **Webcam Pipeline:** Video is streamed in real time, with frame-by-frame landmark detection and annotation.
- **Landmark Smoothing:** Exponential moving averages reduce jitter for stable angle calculations.
- **Angle \& Gesture Estimation:** All major joint angles, wrist/finger motions, and gestures are computed per frame.
- **Feedback Generation:** Feedback messages adapt to your current pose and progress.
- **Session Reports:** When ending a session, Excel and PDF reports are generated and made available for download.


## Example Outputs

- **Excel**: Full time series of tracked angles and gestures.
- **PDF Summary**: Min, max, mean values for all tracked motions vs. clinical normal ranges.
- **Plot PDFs**: Time-series plots for all metrics visualizing your progress.


## Customization

- Adjust analysis thresholds and feedback prompts in `final_code.py`.
- Extend to recognize custom gestures, add user authentication, or support additional analytics.


## Privacy Note

- All processing runs locally by default—video and data stay on your device.
- Session logs and reports are stored in the `outputs/` folder.




<div style="text-align: center">⁂</div>

[^1]: app.py

[^2]: final_code.py

[^3]: index.css

[^4]: live.css

[^5]: results.css

[^6]: index.html

[^7]: live.html

[^8]: results.html

