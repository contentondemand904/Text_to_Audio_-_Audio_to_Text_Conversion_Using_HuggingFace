# **Text-to-Audio and Audio-to-Text Conversion using Hugging Face**

This project demonstrates how to perform text-to-audio and audio-to-text conversions using Hugging Face transformers. It includes examples of generating audio from text, converting audio to text, and downloading audio for further processing.

---

## **Project Overview**
1. **Text-to-Audio Conversion**  
   Use the Hugging Face `pipeline` and the `suno/bark-small` model to convert text into audio.  
2. **Audio-to-Text Conversion**  
   Use the Hugging Face `whisper-medium` model to transcribe audio files into text.  
3. **Download and Play Audio**  
   Download an audio file, play it directly, and process it for transcription.  

---

## **Requirements**
- Python 3.7+
- Hugging Face `transformers` library
- Jupyter Notebook (or Google Colab)
- `IPython` for displaying audio in notebooks

---

## **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>


# **Text-to-Audio and Audio-to-Text Conversion using Hugging Face**

This project demonstrates text-to-audio and audio-to-text conversions using Hugging Face transformers. It includes key models, installation instructions, and code examples for quick implementation.

---

# **Text-to-Audio and Audio-to-Text Conversion using Hugging Face**

This project demonstrates text-to-audio and audio-to-text conversions using Hugging Face transformers. It showcases how to generate audio from text, transcribe audio into text, and play audio directly within a Python environment.

---

## **Installation**

### Install dependencies:
Run the following command to install the required libraries:
```python
pip install transformers ipython
```
---

## **How to Run**

### **Text-to-Audio Conversion**  
Convert text into audio using the `suno/bark-small` model:
```python
from transformers import pipeline
from IPython.display import Audio

# Input text
text = "Subscribe to my channel: Content on Demand"

# Load the text-to-speech pipeline
pipe = pipeline("text-to-speech", model='suno/bark-small')

# Generate audio
output = pipe(text)

# Play the audio
Audio(output["audio"], rate=output["sampling_rate"])
```

---

## **Audio-to-Text Conversion**

### Transcribe audio using the openai/whisper-medium model:

```python
from transformers import pipeline

# Load the Whisper model
whisper = pipeline('automatic-speech-recognition', model='openai/whisper-medium')

# Transcribe the audio file
transcription = whisper('audio.mp3')

# Print the transcription
print(transcription)

```




---

## **Key Models**

-suno/bark-small: Used for converting text into audio.

-openai/whisper-medium: Used for transcribing audio into text.
from transformers import pipeline




## **Acknowledgments**

-Hugging Face for providing powerful transformer-based models.

-Google Colab for offering an easy-to-use platform for running Python code.
