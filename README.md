# 🎤 Audio2Art (Voice to AI Art Generator)

Audio2Art is a complete **Streamlit web application** that converts **voice prompts (WAV audio)** into **AI-generated images** using **Speech Recognition + Stable Diffusion**.

This project allows users to upload an audio command, automatically converts it into text, and generates a creative artwork instantly.

---

## 📌 Project Features

✅ **Voice to Text Conversion (Real-Time)**  
Uploads a WAV file and converts speech → text using Google Speech Recognition.

✅ **AI Image Generation (Stable Diffusion)**  
Generates a high-quality image from the transcribed text prompt.

✅ **Streamlit Web UI (Simple & Clean)**  
Easy-to-use interface with background styling and clear outputs.

✅ **Prompt-Based Creativity**  
Users can generate different artworks based on different voice commands.

---

## 🧠 Workflow Used

1. **Audio Upload**
   - User uploads a `.wav` file using Streamlit file uploader.

2. **Audio Processing**
   - Saves uploaded file temporarily as `input_audio.wav`

3. **Speech-to-Text**
   - Uses `speech_recognition` with Google Speech Recognition API
   - Converts audio → transcribed text prompt

4. **Stable Diffusion Model Loading**
   - Loads model: `runwayml/stable-diffusion-v1-5`
   - Uses Streamlit caching to avoid reloading every time

5. **Image Generation**
   - Transcribed text is passed as a prompt to Stable Diffusion
   - Generated image is saved as `generated_art.png`

6. **Display Output**
   - Shows:
     - Uploaded audio preview
     - Transcribed text
     - Generated artwork image

---

## 📁 Project Structure

Audio2art-main/
├── app.py
├── requirements.txt
├── README.md
└── input_audio.wav



## ⚙️ Installation

### 1) Install Dependencies

 - pip install -r requirements.txt **
## ▶️ Run the Streamlit App
 - If streamlit command is not working, run using:

## bash
## Copy code
 - python -m streamlit run app.py

## 📌 Input in App
 - Users can upload:
 - Voice Command Audio (WAV format)

## Example voice prompt:

 - “A futuristic city at sunset”
 - “A cute cat sitting on the moon”
 - “A beautiful nature landscape with mountains”

## 📊 Output
### The app displays:

 - ✅ Uploaded Audio Preview
 - 📝 Transcribed Text Output
 - 🎨 Generated AI Artwork Image

 - ⚠️ Important Notes
 - ✅ Model Download Size
 - Stable Diffusion model is very large (~5GB+).
 - Make sure you have enough free space.

 - ✅ If C drive is full (Windows Fix)
## You can move HuggingFace cache to another drive (example S drive):

 - powershell
 - Copy code
 - setx HF_HOME "S:\hf_cache"
 - setx HF_HUB_CACHE "S:\hf_cache"
 - setx TRANSFORMERS_CACHE "S:\hf_cache"
 - Restart the terminal and run again.

### ⚠️ CPU vs GPU
 - If CUDA is not available, the model runs on CPU and may take more time to generate images.

## 📦 Dependencies
 - streamlit
 - torch
 - torchaudio
 - diffusers
 - transformers
 - soundfile
 - speechrecognition
 - huggingface_hub
 - accelerate
 - safetensors


## 👩‍💻 Author
 - Audio2Art - Voice to AI Art Generator Project
