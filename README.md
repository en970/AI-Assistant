Ringo - A Multimodal AI Voice Assistant
========================================

Overview
--------
This project is a multimodal voice-activated AI assistant named "Ringo", built with Python. It uses natural speech recognition, image analysis, clipboard extraction, and generative AI models to respond to user prompts.

You activate it by saying "Ringo" followed by your command.

Key Features
------------
- Voice command recognition with wake word ("Ringo")
- Automatic webcam image capture, screenshot, or clipboard extraction based on prompt context
- Image context interpretation using Google Gemini vision API
- Clipboard text analysis
- Generative responses using Groq (LLaMA3) or OpenAI (GPT-4)
- Text-to-speech response with OpenAI TTS (`echo` voice)
- Real-time whisper speech-to-text with FasterWhisper

Setup Instructions
------------------
1. **Install dependencies:**

   Run this command in your virtual environment:
    pip install -r requirements.txt


2. **Install system-level dependencies:**
- Windows users may need to install `portaudio` and `PyAudio`:
  - Download PyAudio wheel: https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyaudio
  - Install with pip:
    ```
    pip install path_to_downloaded_whl_file
    ```

3. **Set your API keys:**
Edit the main Python file and replace the placeholders with your actual API keys:
- GROQ API Key
- Google Gemini API Key
- OpenAI API Key

4. **Run the assistant:**
   python your_script_name.py


Once it starts, say "Ringo" followed by your prompt.

Example Prompts
---------------
- "Ringo, what’s on my clipboard?"
- "Ringo, what do you see on my screen?"
- "Ringo, describe my current appearance from webcam."
- "Ringo, summarize this code from clipboard."

Folder/File Structure
---------------------
- `main.py` .................... Main assistant logic
- `requirements.txt` .......... All required Python packages
- `README.txt` ................ This file
- `screenshot.jpg` ............ Temporary screenshot image
- `webcam.jpg` ................ Temporary webcam image
- `prompt.wav` ................ Temporary audio file for whisper STT

Requirements
------------
- Python 3.10+
- Working microphone and optionally a webcam
- Stable internet connection
- Compatible audio drivers (for PyAudio and SpeechRecognition)

Known Issues
------------
- Microphone errors can occur if the device is in use or misconfigured.
- Webcam must be accessible by OpenCV (`cv2.VideoCapture(0)`).
- Ensure clipboard contains text before using "clipboard" mode.

Credits
-------
- OpenAI API (TTS + GPT)
- Google Gemini Vision API
- Groq LLaMA3
- FasterWhisper
- PyAudio, SpeechRecognition, OpenCV, Pillow

License
-------
MIT License


