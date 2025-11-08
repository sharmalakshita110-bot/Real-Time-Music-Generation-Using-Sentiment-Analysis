# 🎵 Real-Time Music Generation Using Sentiment Analysis

An **AI-driven system** that interprets human facial expressions in real time and dynamically generates **emotion-aligned music** using **deep learning (LSTM)** and **audio synthesis**.

---

## 🌟 Overview

This project integrates **Facial Emotion Recognition (FER)** with **music generation** to create an adaptive emotional experience.  
When a user’s face is captured through a webcam, the model analyzes their dominant emotion (e.g., *happy*, *sad*, *angry*) and generates a short music piece reflecting that emotional tone.

---

## 🧠 Core Features

- 🎭 **Real-Time Emotion Detection** using webcam and `fer` library  
- 🎶 **Emotion-Conditioned Music Generation** via LSTM-based sequence modeling  
- 💾 **Automatic MIDI Creation** with rhythm patterns per emotion  
- 🔊 **MIDI-to-WAV Conversion** for direct playback  
- 🎧 Supports emotions: `happy`, `sad`, `angry`, `surprise`, `fear`, `disgust`, and `neutral`

---
🧩 How It Works
The webcam captures a live image of the user.
FER (Facial Expression Recognition) detects and classifies emotions.
The LSTM model generates a musical sequence reflecting that emotion.
The system composes the piece as a MIDI file and converts it to WAV for playback.
The output audio represents the emotional tone of the detected expression

| Emotion     | Characteristics                        |
| ----------- | -------------------------------------- |
| 😄 Happy    | Fast tempo, major scale, upbeat rhythm |
| 😢 Sad      | Slow tempo, minor scale, soft rhythm   |
| 😠 Angry    | Sharp rhythm, aggressive tone          |
| 😲 Surprise | Varied rhythm, dynamic flow            |
| 😱 Fear     | Tense rhythm, darker scale             |
| 😐 Neutral  | Balanced and calm melody               |


🧰 Tech Stack

Programming Language: Python 3
Libraries Used:
tensorflow — LSTM model for note prediction
pretty_midi — Music generation and MIDI manipulation
fer — Facial emotion recognition
opencv-python — Webcam and image processing
google-colab, IPython — For Colab integration
numpy — Numerical computation

🧑‍💻 Author
Lakshita Sharma
