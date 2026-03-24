# 📞 CityCare Clinic AI

A voice-based AI receptionist for healthcare clinics that handles appointment booking, emergency detection, and call flow using browser speech APIs and n8n workflow automation.

---

## 🚀 Features

- 🎤 Real-time voice interaction (Speech-to-Text + Text-to-Speech)
- 🧠 Multi-turn conversation memory
- 📅 Appointment booking flow
- 🚨 Emergency detection and override system
- ⏰ After-hours handling (9 AM – 6 PM)
- 🔁 Continuous conversation loop

---

## 🏗️ Architecture

Frontend (Browser)
- Web Speech API (STT)
- SpeechSynthesis API (TTS)
- JavaScript (chat memory + UI)

Backend (n8n)
- Webhook node (receives requests)
- HTTP Request node (calls LLM API)
- Respond to Webhook (returns response)

Model
- Llama 3.1 8B (via API)

---

## 🔄 System Flow

User speaks  
→ Speech-to-text (browser)  
→ Send to n8n webhook  
→ n8n calls LLM  
→ Response returned  
→ Text-to-speech output  

---

## 💻 Setup

### 1. Run n8n
```bash
npx n8n
```

### 2. Import Workflow
	•	Open n8n UI
	•	Import n8n-workflow.json

### 3. Run Frontend

Open index.html in browser

## Setup Note
Add your API key inside n8n credentials before running the workflow.

⸻

## 💰 Cost Estimation
	•	~₹0.01 – ₹0.03 per call
	•	~₹10 – ₹30 per 1000 calls

⸻

## 🔮 Future Improvements
	•	Redis-based memory
	•	Conversation summarization
	•	Calendar integration
	•	Multilingual support

⸻

# 📌 Note

This project focuses on workflow design, safety handling, and real-world call scenarios rather than just chatbot responses.
