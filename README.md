

# 1. AI Audio Summarization and Speech Generation

## Overview

This workflow accepts an audio file URL, transcribes the audio using Groq Whisper, summarizes the content using Google Gemini, and converts the summary back into speech using Murf.ai.

---

## Features

* Accepts audio file URLs through chat input
* Downloads and processes audio automatically
* Converts speech to text using Groq Whisper API
* Generates meeting-style summaries using Google Gemini
* Converts summarized text back into AI-generated speech using Murf.ai
* Downloads the final summary audio file

---

## Workflow Architecture

```text
Chat Trigger
     ↓
Set Node (Extract Audio URL)
     ↓
HTTP Request → Download Audio
     ↓
HTTP Request → Groq Whisper Transcription
     ↓
Basic LLM Chain → Google Gemini Summary
     ↓
HTTP Request → Murf.ai Text-to-Speech
     ↓
HTTP Request → Download Final Audio
```

---

## Technologies Used

* n8n
* Groq Whisper API
* Google Gemini API
* Murf.ai API
* HTTP Request Nodes
* Basic LLM Chain

---

## Required API Keys

Before running the workflow, configure:

* Groq API Key
* Google Gemini API Key
* Murf.ai API Key

---

## Setup Instructions

### 1. Import Workflow

* Open n8n
* Click Import Workflow
* Upload the exported JSON file

---

### 2. Configure Credentials

Add the following credentials inside n8n:

* Google Gemini API
* Groq API
* Murf.ai API

---

### 3. Execute Workflow

Run the workflow and provide an audio file URL in chat.

Example:

```text
https://example.com/audio.mp3
```

---

## Summarization Prompt

```text
- Start each point with an action verb when possible
- Zero decorative language

FORMAT:
- Point one
- Point two
- Point three

BEGIN SUMMARIZATION:
{{ $json.text }}
```

---

## Expected Output

The workflow generates:

* Audio transcription
* Structured meeting summary
* AI-generated speech summary in MP3 format

---

## Common Issues

### Groq API Error

Ensure:

* Audio file downloads correctly
* Binary property is named correctly
* Whisper model is configured properly

---

### Murf.ai Audio Generation Failure

Check:

* API key validity
* Voice ID configuration
* JSON body formatting

---

## Future Improvements

* Multi-language transcription
* Speaker diarization
* Real-time streaming support
* Email delivery integration

---

