🚀 Live Meeting Summarizer Application
An AI-powered web application that converts meeting audio into structured summaries with speaker identification and actionable insights.

🌐 Live Demo
👉 https://live-meeting-summarizer-application.vercel.app

📌 Features
🎤 Real-time Speech-to-Text (Whisper)
🧑‍🤝‍🧑 Speaker Diarization (Pyannote)
🧠 AI-based Summarization (LLaMA 3 via Groq API)
📄 Structured summaries with key decisions & action items
💾 Save, download, and manage meeting history

⚙️ Tech Stack

Frontend: React.js, Vite, CSS
Backend: Python, FastAPI
Database: MongoDB Atlas

AI Models:

Whisper (Speech-to-Text)
Pyannote (Diarization)
LLaMA 3 (Summarization via Groq API)

Deployment:

Vercel (Frontend)
Hugging Face Spaces (Backend)

🔄 Workflow
User records/uploads audio
Audio sent to backend
Whisper → converts speech to text
Pyannote → identifies speakers
LLM → generates summary + action items
Data stored in MongoDB
Results displayed on dashboard
🎯 Impact
Saves time by eliminating manual note-taking
Improves accountability with speaker tracking
Makes meetings searchable and structured

👩‍💻 Author

Aashika Arunkumar
