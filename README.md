# Emotion Detection Web App

## Description

This project is the final assignment for the **"AI-Based Web Application Development and Deployment"** course (IBM / Coursera). It is a Flask web application that uses **IBM Watson NLP** to analyze a given text and detect the dominant emotion expressed in it — anger, disgust, fear, joy, or sadness.

The application takes text input from a user through a simple web interface, sends it to the Watson NLP Emotion Predict service, and returns a formatted response showing the score for each emotion along with the dominant one.

## Features

- **Emotion detection** using IBM Watson NLP's Emotion Predict API
- **Flask-based REST endpoint** (`/emotionDetector`) that processes text and returns structured results
- **Web interface** for entering text and viewing results in real time
- **Error handling** for blank or invalid input, returning a clear message instead of crashing
- **Unit tests** verifying accurate detection across all five emotions
- **Packaged as a Python module** (`EmotionDetection`) for reusability
- **Pylint-compliant code** (10/10 static code analysis score) with full docstring documentation

## Technologies Used

- Python 3
- Flask
- IBM Watson NLP (Emotion Predict service)
- Requests library
- unittest (for testing)
- Pylint (for static code analysis)

## Project Structure

```
final_project/
├── EmotionDetection/
│   ├── __init__.py
│   └── emotion_detection.py
├── templates/
│   └── index.html
├── static/
│   └── mywebscript.js
├── server.py
└── test_emotion_detection.py
```

## How It Works

1. The user enters a statement in the web interface.
2. The Flask server sends the text to the Watson NLP Emotion Predict API.
3. The API returns scores for **anger**, **disgust**, **fear**, **joy**, and **sadness**.
4. The application identifies the **dominant emotion** (the one with the highest score) and displays a formatted response to the user.

## Installation and Usage

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd final_project
   ```

2. Install the required dependencies:
   ```bash
   pip install flask requests
   ```

3. Run the application:
   ```bash
   python3 server.py
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:5000
   ```

5. Enter a statement in the text field and click **Run Sentiment Analysis** to see the detected emotions.

## Running Tests

To run the unit tests and verify the emotion detection logic:

```bash
python3 test_emotion_detection.py
```

## Static Code Analysis

This project follows PEP8 standards and has been validated with Pylint:

```bash
pylint server.py
```

**Result:** 10.00/10
