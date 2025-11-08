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
Webcam Capture:
The notebook uses OpenCV to continuously capture live video frames from your webcam.

Emotion Detection:
Each frame is analyzed using the FER (Facial Emotion Recognition) model, which identifies the dominant facial emotion — for example, happy, sad, or angry.

Emotion Mapping:
The detected emotion determines the musical mood parameters such as tempo, pitch range, and scale type (major/minor).

Happy → Fast tempo, major scale
Sad → Slow tempo, minor scale
Angry → High intensity, dissonant tone
Neutral → Balanced melody
Music Generation:
Based on the chosen parameters, the system generates a MIDI sequence.
It uses randomized or LSTM-guided note patterns to simulate expressive and emotion-aligned music.

Audio Conversion:
The generated MIDI is converted into a WAV audio file using FluidSynth, allowing playback directly within the notebook.

Playback:
The final audio file is automatically played within the notebook, giving the user real-time feedback matching their current emotional state.

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

💻 Code Explanation 

The entire project runs inside a single Jupyter Notebook structured as follows:

1. Environment Setup
Installs all necessary dependencies such as opencv-python, fer, pretty_midi, and pyfluidsynth to enable webcam capture, emotion recognition, and MIDI-to-WAV conversion.

2. Initialization
Loads essential libraries, initializes the webcam, and sets up the FER emotion detector.

3. Emotion Detection Module
Uses the FER model to process each webcam frame and extract emotion probabilities. The most dominant emotion is selected as the current mood input for the generator.

4. Emotion-to-Music Mapping
Defines the logic that links emotions to musical properties:
Tempo (speed of the music)
Scale type (major/minor)
Pitch range (high or low notes)
Rhythmic intensity (smooth or sharp)

5. Music Generation Engine
Creates a sequence of musical notes and durations that match the emotional profile. This stage mimics human composition by balancing randomness with emotion-guided rules.

6. MIDI & Audio Rendering
The generated sequence is converted into a MIDI file using PrettyMIDI, then rendered into an audible WAV file using FluidSynth.

7. Output Playback
The WAV file is automatically played within the notebook, producing music that corresponds to the user’s live-detected emotio

🧑‍💻 Author
Lakshita Sharma
