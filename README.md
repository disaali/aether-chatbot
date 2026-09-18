# Aether · Groq Chat

A cinematic streaming chat UI on top of Groq. Animated aurora background, conversation memory, and live token streaming.

## Setup

```bash
cd groq-chat
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
```

Put your real key in `.env`:

```
GROQ_API_KEY=gsk_...
GROQ_MODEL=openai/gpt-oss-120b
```

## Run

```bash
uvicorn app:app --reload --port 8000
```

Open [http://127.0.0.1:8000](http://127.0.0.1:8000).

Enter sends. Shift+Enter makes a new line. Chats are stored in the browser.
