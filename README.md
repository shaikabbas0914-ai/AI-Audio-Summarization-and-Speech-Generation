# 🎧 AI Audio Summarization & Speech Generation Workflow

<div align="center">

![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-orange?style=for-the-badge&logo=n8n)
![Groq](https://img.shields.io/badge/Groq-Whisper%20API-black?style=for-the-badge)
![Gemini](https://img.shields.io/badge/Google-Gemini%20AI-blue?style=for-the-badge&logo=google)
![Murf AI](https://img.shields.io/badge/Murf.ai-Text%20to%20Speech-purple?style=for-the-badge)
![AI](https://img.shields.io/badge/AI-Audio%20Summarization-green?style=for-the-badge)

### 🚀 AI-Powered Audio Transcription, Summarization & Speech Generation

Transcribe • Summarize • Convert • Download Audio Automatically

</div>

---

# 📌 Project Overview

This workflow is an AI-powered audio processing pipeline built using:

- :contentReference[oaicite:0]{index=0}
- Groq Whisper API
- Google Gemini
- Murf.ai

The workflow accepts an audio file URL, transcribes the audio using Groq Whisper, summarizes the content using Google Gemini, and converts the summary back into realistic AI-generated speech using Murf.ai.

---

# ⚡ Workflow Process

The workflow automates the following steps:

🎵 Accept Audio File URL  
⬇️ Download Audio Automatically  
📝 Transcribe Audio using Groq Whisper  
🤖 Generate AI Summary using Gemini  
🔊 Convert Summary to AI Speech using Murf.ai  
📥 Download Final MP3 Summary Audio  

---

# 🧠 Features

✨ Audio-to-text transcription  
✨ AI-powered summarization  
✨ Text-to-speech conversion  
✨ Fully automated workflow  
✨ Downloadable summary audio  
✨ Meeting-style concise summaries  
✨ AI-generated natural voice narration  
✨ Easy integration with APIs  

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| 🔄 n8n | Workflow Automation |
| 🎤 Groq Whisper API | Speech-to-Text Transcription |
| 🤖 Google Gemini API | AI Summarization |
| 🔊 Murf.ai API | Text-to-Speech Generation |
| 🌐 HTTP Request Nodes | API Integration |
| 🧠 Basic LLM Chain | AI Processing |

---

# 🏗️ Workflow Architecture

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

# ⚙️ Workflow Explanation

# 1️⃣ Chat Trigger

The workflow begins using a **Chat Trigger Node**.

## Purpose

Allows users to provide an audio file URL as input.

## Example Input

```text
https://example.com/audio.mp3
```

---

# 2️⃣ Set Node — Extract Audio URL

The Set Node extracts and stores the audio URL provided by the user.

## Responsibilities

✅ Stores input URL  
✅ Passes URL to the download node  
✅ Prepares workflow variables  

---

# 3️⃣ Download Audio File

An HTTP Request node downloads the audio file automatically.

## Purpose

Fetches the audio file from the provided URL.

## Output

🎵 Binary audio file ready for transcription.

---

# 4️⃣ Groq Whisper Transcription

The workflow uses the Groq Whisper API for speech-to-text conversion.

## Features

✅ Fast transcription  
✅ Accurate speech recognition  
✅ Handles long audio inputs  
✅ Supports multiple audio formats  

---

# 🎤 Whisper Model Processing

The downloaded audio is sent to Groq Whisper using an HTTP Request node.

## Output

📝 Complete audio transcription text.

---

# 5️⃣ AI Summarization using Gemini

The transcribed text is summarized using Google Gemini.

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

## Features

✅ Concise summaries  
✅ Meeting-style formatting  
✅ Structured bullet points  
✅ Action-oriented outputs  

---

# 6️⃣ Murf.ai Text-to-Speech

The summarized text is converted back into speech using Murf.ai.

## Features

🔊 Natural AI-generated voice  
🔊 MP3 audio generation  
🔊 Multiple voice options  
🔊 Realistic narration quality  

---

# 🎙️ Recommended Voice IDs

| Voice ID | Description |
|-----------|-------------|
| en-US-natalie | Female, American |
| en-US-davis | Male, American |
| en-GB-oliver | Male, British |

---

# 7️⃣ Download Final Audio

The final HTTP Request node downloads the generated MP3 summary audio file.

---

# 📂 Final Output

The workflow generates:

✅ Audio transcription  
✅ Structured summary  
✅ AI-generated speech summary  
✅ Downloadable MP3 file  

---

# ▶️ Setup Instructions

# Step 1 — Import Workflow

1️⃣ Open n8n  
2️⃣ Click **Import Workflow**  
3️⃣ Upload the exported JSON workflow file  

---

# Step 2 — Configure Credentials

Add the following credentials inside n8n:

✅ Google Gemini API  
✅ Groq API  
✅ Murf.ai API  

---

# Step 3 — Execute Workflow

Run the workflow and provide an audio URL.

## Example

```text
https://example.com/audio.mp3
```

---

# 🔐 Required API Keys

Before running the workflow, configure:

🔑 Groq API Key  
🔑 Google Gemini API Key  
🔑 Murf.ai API Key  

---

# 📸 Suggested Screenshots

Add these screenshots to improve your repository:

📷 Workflow Canvas  
📷 Groq Whisper Configuration  
📷 Gemini LLM Setup  
📷 Murf.ai HTTP Request Node  
📷 Final MP3 Output  

---

# 💡 Example Use Cases

🎙️ Podcast Summarization  
📚 Lecture Summaries  
🧠 Meeting Notes Automation  
📰 Audio News Briefs  
🎓 Educational Content Processing  
📞 Call Transcription & Summaries  

---

# 🧩 n8n Nodes Used

| Node | Purpose |
|------|----------|
| Chat Trigger | User Input |
| Set Node | Extract Audio URL |
| HTTP Request | Download Audio |
| HTTP Request | Groq Whisper API |
| Basic LLM Chain | AI Summarization |
| Google Gemini Chat Model | AI Reasoning |
| HTTP Request | Murf.ai Text-to-Speech |
| HTTP Request | Download MP3 |

---

# 📈 Benefits of This Workflow

🚀 Automates audio summarization  
🚀 Saves manual transcription effort  
🚀 Generates concise actionable summaries  
🚀 Converts summaries into speech automatically  
🚀 Improves productivity using AI automation  

---

# 🔮 Future Improvements

✅ Multi-language transcription  
✅ Speaker diarization  
✅ Real-time streaming support  
✅ Email delivery integration  
✅ Background music generation  
✅ Podcast-style narration  
✅ Translation support  
✅ Voice emotion customization  

---

# ⚠️ Common Issues

# ❌ Groq API Error

## Ensure:

✅ Audio downloads correctly  
✅ Binary property name is configured properly  
✅ Whisper model settings are correct  

---

# ❌ Murf.ai Audio Generation Failure

## Check:

✅ API key validity  
✅ Voice ID configuration  
✅ JSON request formatting  

---

# ⚠️ Limitations

⚠️ Requires valid API keys  
⚠️ Long audio files may increase processing time  
⚠️ Audio quality depends on input clarity  
⚠️ Free-tier APIs may have usage limits  

---

# 📚 Learning Outcomes

By building this project, you will learn:

✅ AI workflow automation using n8n  
✅ Groq Whisper integration  
✅ Google Gemini summarization workflows  
✅ Murf.ai text-to-speech automation  
✅ API orchestration using HTTP Request nodes  
✅ AI prompt engineering  
✅ Audio AI pipeline design  

---

# 👨‍💻 Author

Built with ❤️ using AI Workflow Automation, Groq Whisper, Gemini AI, and Murf.ai

---

# 🌟 Show Your Support

If you like this project:

⭐ Star the repository  
🍴 Fork the project  
📢 Share with others  

---

# 📚 Useful Resources

- [n8n Official Website](https://n8n.io?utm_source=chatgpt.com)
- [Groq API Documentation](https://console.groq.com/docs?utm_source=chatgpt.com)
- [Google Gemini API Documentation](https://ai.google.dev?utm_source=chatgpt.com)
- [Murf.ai Official Website](https://murf.ai?utm_source=chatgpt.com)

---



# 🎧 AI + Audio + Automation = Smart Speech Intelligence

</div>
