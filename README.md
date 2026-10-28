# Neural Vision

A browser-based emotion and gesture recognition demo that uses your webcam to detect facial expressions and hand movements in real time.

This project is a single-file HTML experience that blends:
- Face detection and emotion recognition using `@vladmandic/face-api`
- Hand landmark tracking using `@mediapipe/hands`
- Real-time visualization with interactive UI panels and live metrics

It is designed to run locally in the browser without a backend or model training pipeline.

## Live Demo

Open the app directly in your browser after downloading or cloning the repository.

## Features

- Real-time face detection from webcam feed
- Emotion classification with confidence scores
- Hand gesture recognition for common gestures and finger counting
- Dual-hand detection and combined gesture analysis
- Live FPS and detection counters
- Stylish dark UI inspired by futuristic surveillance dashboards
- Works entirely in-browser with CDN-hosted libraries

## Project Overview

This repository contains a single interactive page:

- `emotion_detector.html` — complete frontend application with HTML, CSS, JavaScript, and embedded logic

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Face API (`@vladmandic/face-api`)
- MediaPipe Hands (`@mediapipe/hands`)

## How It Works

1. The application requests camera access from the browser.
2. A face detection model identifies faces in the video feed.
3. Expression predictions are smoothed over time for stable emotion classification.
4. A hand tracking model recognizes landmarks and estimates finger states and gestures.
5. The UI renders the live webcam, bounding boxes, confidence bars, and gesture summaries.

## Run Locally

### Option 1: Open directly in a browser

1. Clone the repository.
2. Open `emotion_detector.html` in a modern browser.
3. Allow camera permission when prompted.

Note: Some browsers may restrict camera access when directly opening a local file. Serving over a local web server is the most reliable method.

### Option 2: Use a local web server

From the project folder:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/emotion_detector.html
```

## Recommended Browser

- Chrome
- Edge
- Brave

A local HTTP server is recommended for best compatibility with webcam access.

## Notes

- The app relies on browser access to your camera and internet access to fetch model files and JavaScript libraries from CDNs.
- Accuracy depends on lighting, camera quality, and face visibility.
- Emotion recognition is estimated from facial expression patterns and is not a substitute for medical or psychological analysis.

## Repository Structure

```text
Motion-Detection/
├── emotion_detector.html
└── README.md
```

## Future Enhancements

Potential improvements include:
- Better emotion smoothing and confidence calibration
- More gesture categories and custom actions
- Voice or text output for detected emotions
- Mobile-responsive optimization
- Exporting analytics or session summaries

## License

This project is provided as-is for educational and demonstration purposes. If you plan to use it commercially or in production, review the licensing terms of the third-party libraries used by the project.

## Author

Built for real-time computer vision experimentation and interactive demos.
