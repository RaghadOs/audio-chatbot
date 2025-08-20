# Voice AI Chatbot 🤖

This project demonstrates a full pipeline for converting speech to text, 
generating an AI response using Cohere, and converting that response back to audio.  

## Features
- 🎤 **Speech-to-Text**: Converts `.wav` input into text using Whisper or Google Speech Recognition.  
- 🧠 **AI Response**: Uses Cohere's `command-r` model to generate contextual replies.  
- 🔊 **Text-to-Speech**: Outputs the AI's reply as audio using Google TTS (`gTTS`).  

## Requirements
Install dependencies:
```bash
pip install speechrecognition cohere gTTS pydub
```

Also install FFmpeg (needed by pydub):
```bash
sudo apt-get install ffmpeg
```

## Usage
1. Place your input audio as input.wav (mono/stereo, 16-bit PCM).
2. Run the script:
```bash
audio_chatbot_code.ipynb
```
3. The pipeline will:
- Extract text from your audio
- Generate a reply with Cohere
- Save the AI reply as reply.mp3

## Example
# Input (speech):
```bash
السلام عليكم ورحمة الله وبركاته
```
# Extracted Text:
```bash
السلام عليكم ورحمة الله وبركاته
```
# AI Reply:
```bash
وعليكم السلام ورحمة الله وبركاته، أهلاً بك في مساعدك الشخصي! كيف يمكنني مساعدتك اليوم؟
```
# Output Audio:
An MP3 file (reply.mp3) with the spoken response.

## Notes
- You need a Cohere API Key from Cohere Dashboard.
- Replace COHERE_API_KEY in the script with your own key.
