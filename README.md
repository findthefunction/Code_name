### 陈道锐

## Offline Translator for Speech and Text via Pictures/PDFs on Orange Pi Plus
This project aims to develop an offline translator capable of translating speech and text from pictures and PDFs. The solution is designed to run on an Orange Pi Plus with 32GB of RAM, utilizing various Python packages for image recognition and translation, alongside Ollama AI models for offline processing.

# System Overview
The system integrates hardware and software components to capture, process, and translate speech and text from various inputs, including live speech, pictures, and PDF documents. The core functionalities include speech recognition, optical character recognition (OCR), language translation, and text-to-speech (TTS) conversion, all running offline on an Orange Pi Plus device.

# Hardware Requirements
Orange Pi Plus with 32GB of RAM
MicroSD Card (128GB recommended for storage of AI models and libraries)
Camera Module (for capturing images of text)
Microphone and Speaker (for speech input and output)
Software Requirements
Operating System: Armbian or a compatible Linux distribution for Orange Pi Plus
Python 3.8+: The primary programming language for developing the application
Tesseract OCR: For optical character recognition
Ollama AI Models: For offline speech recognition and translation models
Additional Python packages: numpy, Pillow, pytesseract, speech_recognition, gTTS (Google Text-to-Speech), opencv-python for image processing.
Installation and Setup
Prepare Orange Pi Plus:

Install Armbian or another compatible Linux OS on your Orange Pi Plus.
Ensure your device is updated: sudo apt-get update && sudo apt-get upgrade
Install Python and Dependencies:

Install Python 3.8+: sudo apt-get install python3.8
Install pip: sudo apt-get install python3-pip
Install Required Python Packages:

pip3 install numpy Pillow pytesseract speech_recognition gTTS opencv-python
Install Tesseract OCR:

sudo apt-get install tesseract-ocr
Download and Configure Ollama AI Models:

Download the required Ollama AI models for speech recognition and translation.
Note: Ensure compliance with Ollama's guidelines for offline use.
Hardware Configuration:

Connect the camera module and test it with fswebcam or similar tools.
Connect the microphone and speaker, testing them with arecord and aplay respectively.
Development
Speech Recognition Module
Use Ollama AI models integrated with the speech_recognition library for offline speech recognition.
OCR and Image Processing
Capture images using the camera module.
Process images with opencv-python to enhance text visibility.
Apply pytesseract for text extraction from images and PDFs.
Translation Module
Integrate Ollama AI translation models to translate the extracted text or recognized speech into the desired language.
Text-to-Speech (TTS)
Convert translated text back into speech using gTTS for output through the speaker.
Running the Application
Speech Translation:
Activate the speech recognition module to capture and translate speech.
Image/PDF Translation:
Use the camera module to capture images or upload PDFs.
Process images/PDFs through the OCR module to extract text.
Translate the extracted text into the desired language.
Conclusion
This README outlines the foundational steps to create an offline translator on an Orange Pi Plus device. 
The project integrates hardware components with Python-based software solutions, utilizing advanced AI models for comprehensive speech and text translation functionalities. 
