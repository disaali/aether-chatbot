# Aether · Groq Chat

Aether is a small AI chat app built for me and a few friends, no accounts, no tracking, no fuss. It's a clean, fast interface for talking to an AI, powered by Groq's LLM API under the hood so responses stream in almost instantly instead of the slow typing effect you get on most chat apps.

There's no heavy backend or database. Conversations stay in your browser and aren't stored anywhere else. You can pick between a few different models depending on what you need. A quick, snappy one for everyday questions, or a slower "thinking" one for anything that needs more reasoning. The interface itself has a simple, dark, aurora style animated background and supports live token streaming as the AI writes its reply.

This was built as a private playground rather than a public product just a way to have our own AI chat space without depending on someone else's app, rate limits, or UI choices.

## Features
- Real-time streaming responses (Server-Sent Events)
- Multiple model options — fast vs. deep reasoning
- Adjustable temperature and max token settings
- Clean, minimal, animated interface
- No sign-up, no accounts, no server-side chat storage — everything lives in your browser

## Tech Stack
- **Backend:** FastAPI (Python)
- **AI Provider:** Groq API
- **Frontend:** Vanilla HTML/JS, no framework
- **Streaming:** Server-Sent Events (SSE)

## Setup

\`\`\`bash
cd groq-chat
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
\`\`\`

Add your Groq API key to `.env`:

\`\`\`
GROQ_API_KEY=gsk_...
GROQ_MODEL=openai/gpt-oss-120b
\`\`\`

## Run

\`\`\`bash
uvicorn app:app --reload --port 8000
\`\`\`

Open [http://127.0.0.1:8000](http://127.0.0.1:8000).

Enter sends a message. Shift+Enter adds a new line. Chats are stored only in your browser session — nothing is saved server-side.

## Deployment
This app needs a Python-capable host (it won't run on plain PHP/shared hosting). It's currently deployed on [Render](https://render.com), with a custom domain pointed at it via CNAME.
