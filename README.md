# Multimodal Emotion Detection with Face + Voice AI

This project combines **real-time facial emotion detection** using [DeepFace](https://github.com/serengil/deepface) with **tone-of-voice analysis** using a pretrained [Wav2Vec2 model](https://huggingface.co/superb/wav2vec2-large-superb-er) from Hugging Face. It captures data from your webcam and microphone, overlays live predictions on the video feed, and updates every few seconds.

---

## Features

- Real-time **face detection and emotion classification**
- Real-time **voice tone analysis**
- Multithreaded microphone processing (no lag!)
- Combined overlay on live webcam stream
- Uses fully **pretrained** models — no training required

---

## Technologies Used

- `DeepFace` – facial expression detection
- `Wav2Vec2` from Hugging Face – tone/emotion from audio
- `PyAudio` – live microphone input
- `OpenCV` – camera display and UI overlay
- `Transformers` – model inference
- `Threading` – for parallel audio processing

---

## Installation

Create and activate a Python environment (recommended):

```bash
conda create -n emotionAI python=3.9
conda activate emotionAI
```

Install dependencies

```pip install opencv-python deepface pyaudio numpy soundfile torch torchaudio transformers```


If `pyaudio` fails on macOS (Apple Silicon), install portaudio first:

```brew install portaudio
export LDFLAGS="-L/opt/homebrew/lib"
export CPPFLAGS="-I/opt/homebrew/include"
pip install pyaudio
```

---
## Running
```python multimodal_emotion.py```

You’ll see:

- Bounding boxes around detected faces

- Facial emotion label with confidence %

- Voice tone label with confidence % in the top-left corner

Press `ESC` to quit.

---
## References
[DeepFace Github](https://github.com/serengil/deepface)

[Hugging Face Model - superb/wav2vec2-large-superb-er](https://huggingface.co/superb/wav2vec2-large-superb-er)

[PyAudio Doc](https://people.csail.mit.edu/hubert/pyaudio/)

---

## Presentation
[Demo Video](https://www.youtube.com/watch?v=8rnxNbSBVZk)

[Pitch](https://www.canva.com/design/DAGtLoXGC90/JeZ24kL22ty-wP8uswpYIw/view?utm_content=DAGtLoXGC90&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h5fef0f45c8)

---
## Credit

Built by [cctz123](https://github.com/cctz123) for the Wharton SF AI Leadership Final Project.





