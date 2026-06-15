# Voice Controlled Automated System 🎙️🤖

An intelligent voice-command pipeline that listens, understands Arabic speech, and triggers automated actions, originally developed to command physical robotic systems.

## 🚀 Project Overview

Hands-free control is crucial for robotics, smart home systems, and accessibility tools. This project builds a localized Voice Communication System capable of processing real-time microphone input, transcribing it using Google's Speech Recognition API, and mapping specific keywords to automated execution logic.

The system is specifically tailored to recognize Arabic commands (e.g., "ابدأ" for Start, "توقف" for Stop) and provides audible text-to-speech (TTS) feedback to confirm the action.

## ⚙️ Methodology

1. **Audio Capture**: Utilizes `SpeechRecognition`'s `Microphone` class to actively listen to the environment and capture raw audio data.
2. **Speech-to-Text (STT)**: 
   - Audio chunks are sent to the Google Web Speech API via `recognize_google`.
   - The language parameter is explicitly set to `ar-EG` (Egyptian Arabic) to accurately capture local dialects and pronunciation.
3. **Command Parsing**: The transcribed text is passed through conditional logic to detect trigger keywords.
4. **Text-to-Speech (TTS) Feedback**:
   - The system utilizes `pyttsx3`, an offline text-to-speech engine, to verbally confirm the recognized command (e.g., "Patrol started", "Scanning the area").
   - This provides a closed-loop system where the user immediately knows if their command was successful.

## 🛠️ Tech Stack & Libraries Used

- **Speech Recognition:** `SpeechRecognition` (Google API)
- **Text-to-Speech:** `pyttsx3`
- **Audio Processing:** `PyAudio`

## 📈 Key Outcomes

- Successfully integrated real-time Arabic speech recognition with programmatic triggers.
- Achieved a highly robust fallback mechanism to gracefully handle unrecognized speech (`UnknownValueError`) or network drops (`RequestError`).

---
*This repository is part of my AI Engineer / Data Scientist Portfolio.*
