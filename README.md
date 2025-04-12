# Hybrid-Speech-Recognition
# Speech Recognition and Sentiment Analysis Project

This project is a voice-based interface that allows users to:
- Record audio input via microphone.
- Perform speech recognition on the recorded audio.
- Classify the recognized text using a Naive Bayes model.
- Analyze sentiment using TextBlob.

It is implemented in a Jupyter Notebook environment using Python, and leverages interactive widgets (ipywidgets) to create a user-friendly interface.

---

## Features

- Record 5-second audio clips using your microphone.
- Convert recorded speech to text using Google Web Speech API.
- Classify spoken input into intent categories (command/question + polarity).
- Perform sentiment analysis (Positive, Neutral, Negative).
- Run everything directly in a Jupyter Notebook with dynamic output.

---

## Dependencies

Make sure the following Python libraries are installed:

```bash
pip install ipywidgets
pip install sounddevice
pip install scipy
pip install SpeechRecognition
pip install scikit-learn
pip install textblob
pip install nltk
```
Also, download the required NLTK dataset:
import nltk
nltk.download('punkt')

## How It Works
-Audio Recording 
Clicking the "Record" button triggers a 5-second microphone recording using the sounddevice library.
The recording is saved locally as output.wav.

-Speech Recognition
When the "Recognize Speech" button is clicked, the recorded audio is processed using the Google Web Speech API via the speech_recognition library.
The audio is converted to text and displayed.

-Text Classification
A Naive Bayes classifier (trained on a small dataset of example phrases) is used to classify the recognized speech.
Categories include command or question with associated polarity (e.g., command-positive, question-neutral).

-Sentiment Analysis
The recognized text is passed to TextBlob for sentiment analysis.
Polarity scores are calculated and categorized as Positive, Neutral, or Negative.

-Dynamic Output Display
All messages and classifications are shown in real-time within the notebook using ipywidgets and IPython.display.
