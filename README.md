# AI-based Text-to-Speech (TTS) Tool

This project is an AI-powered Text-to-Speech (TTS) tool that supports multiple languages and voices. 
It utilizes **Coqui TTS**, an open-source library, to generate natural-sounding speech from text input. 
The tool allows users to choose between English and French languages and outputs the generated audio in `.wav` format.

## Features
- **AI-based Speech Generation**: Uses pre-trained models (Tacotron2) for natural-sounding speech.
- **Multi-language Support**: Currently supports English and French.

## Prerequisites
- Python 3.8 or higher
- `pip` for package installation
- `ffmpeg` installed and added to the system path (required for audio processing)



## Approach and Models Used

### **Tacotron2**
- **Tacotron2** is a state-of-the-art text-to-speech synthesis model developed by Google. It uses a sequence-to-sequence model to map input text to spectrograms (a visual representation of the sound wave). These spectrograms are then converted into speech using a vocoder model, such as **WaveGlow** or **HiFi-GAN**.
  
  In this project, we leverage pre-trained Tacotron2 models for English and French languages. The model uses a sequence-to-sequence approach, where the input is processed and converted into an intermediate spectrogram, which is then converted into a human-like voice.

### **Coqui TTS**
- **Coqui TTS** is an open-source project that provides pre-trained TTS models, including Tacotron2, trained on various datasets in different languages. We use Coqui TTS's pre-trained models to generate speech in both English and French.

  For the English language, the `ljspeech` dataset is used, and for French, the `mai` dataset is used. Both datasets have high-quality recordings to train the models and provide clear, natural-sounding voices.

### **Vocoder (WaveGlow or HiFi-GAN)**
- **WaveGlow** or **HiFi-GAN** are vocoder models that generate audio waveforms from the spectrograms produced by Tacotron2. These vocoders ensure that the generated speech is smooth and free from artifacts, making it sound natural.
