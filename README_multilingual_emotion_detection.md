
# 🗣️ Multilingual Emotion Detection in Voice

This project combines **speech recognition** and **emotion detection** from audio, enabling systems to understand not just *what* is being said, but also *how* it is being said — across multiple languages.

## 📌 Features

- 🎙️ **Transcription using OpenAI's Whisper model**
- 🌍 **Automatic language detection**
- 🎧 **Audio feature extraction (MFCCs + pitch)**
- 🤖 **Emotion classification using an SVM classifier**
- 🎥 **Video-to-audio conversion (MP4 to WAV)**
- 🧠 End-to-end pipeline: from raw voice input to emotion-aware transcription

## 🧰 Technologies Used

- [OpenAI Whisper](https://github.com/openai/whisper) – for multilingual speech recognition
- `librosa` – for audio processing and feature extraction
- `scikit-learn` – for training the emotion classifier
- `moviepy` – for converting MP4 to WAV
- `numpy` – for numerical computations

## 📦 Installation

```bash
pip install openai-whisper librosa scikit-learn moviepy
```

## 🚀 Usage

```python
# Step 1: Train the Emotion Classifier
emotion_classifier, label_encoder = train_emotion_classifier()

# Step 2: Analyze an audio file (MP4)
emotion_aware_speech_recognition("/path/to/audio.mp4")
```

Example output:

```
Detected Emotion: happy
Transcription: I'm so excited to see you!
Language Detected: en
```

## 🧪 How It Works

1. **Convert** MP4 to WAV using `moviepy`.
2. **Transcribe** the audio using Whisper (text + language).
3. **Extract** MFCC and pitch features from audio using `librosa`.
4. **Predict** emotional state using a trained SVM.
5. **Print** the emotion, transcript, and detected language.

## 🔬 Limitations & Future Work

- The emotion classifier is currently trained on **random synthetic data**. For practical use, real labeled emotional audio data (e.g., RAVDESS, CREMA-D) should be used.
- Current emotion categories: `happy`, `sad`, `angry`, `neutral`
- Only MP4 input supported — can be extended to other formats.

## 📁 Example File Structure

```
/your-project
  ├── multilingual_emotion_detection_in_voice.ipynb
  ├── /content
  │    └── happy voice.mp4
```
