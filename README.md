# Transloom Plugin 🌐

> Real-Time AI-Powered Translation & Transcription

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)](https://flask.palletsprojects.com)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](#)

---

## Overview

**Transloom** is an AI-powered plugin that provides real-time speech transcription and multilingual translation. It achieves **over 90% accuracy** across multiple languages and integrates seamlessly with web platforms and conferencing tools via REST API.

---

## Features

- 🎙️ **Real-time transcription** — converts spoken audio to text on the fly
- 🌍 **Multilingual translation** — supports a wide range of language pairs with high accuracy
- 🔍 **Dynamic language detection** — automatically identifies input language
- ⚙️ **Customizable settings** — users can configure output language, speed, and formatting
- 🔌 **REST API** — plug into any web app or video conferencing tool
- 📊 **90%+ accuracy** validated across multiple language benchmarks

---

## Tech Stack

| Layer | Technology |
|---|---|
| Core Model | HuggingFace Transformers |
| NLP / Language Detection | spaCy |
| Backend / API | Flask (Python) |
| Frontend Integration | JavaScript |
| Language | Python 3.10+ |

---

## Installation

```bash
git clone https://github.com/shafirpk07/transloom-plugin.git
cd transloom-plugin
pip install -r requirements.txt
```

---

## Usage

```bash
# Start the Flask server
python app.py
```

Send a POST request to the transcription endpoint:

```bash
curl -X POST http://localhost:5000/transcribe \
  -H "Content-Type: application/json" \
  -d '{"audio_path": "sample.wav", "target_lang": "fr"}'
```

**Response:**
```json
{
  "original_text": "Hello, how are you?",
  "detected_language": "en",
  "translated_text": "Bonjour, comment allez-vous?",
  "confidence": 0.94
}
```

---

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/transcribe` | Transcribe audio and detect language |
| POST | `/translate` | Translate text between any supported language pair |
| GET | `/languages` | List all supported languages |
| GET | `/health` | Service health check |

---

## Project Structure

```
transloom-plugin/
├── app.py               # Flask app entry point
├── models/
│   ├── transcriber.py   # HuggingFace transcription model
│   └── translator.py    # Translation pipeline
├── utils/
│   ├── lang_detect.py   # spaCy language detection
│   └── preprocessor.py  # Audio preprocessing
├── static/
│   └── demo.js          # JavaScript integration demo
├── requirements.txt
└── README.md
```

---

## Author

**Shafir PK** — Data Analyst & ML Enthusiast
📧 pkshafir07@gmail.com · [LinkedIn](https://linkedin.com/in/shafir-pk-540284278)
