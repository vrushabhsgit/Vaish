# Vaish

> A personal AI companion built for genuine connection, conversation, and companionship.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue)](https://www.python.org/)
[![Status](https://img.shields.io/badge/status-in%20development-orange)]()

Vaish is a personal AI companion project. It is designed as an always-available conversational partner for someone who spends most of their time working on a laptop and wants someone to talk to, share thoughts with, and feel connected to.

This is a personal project. It is being built as both a practical companion and a way to practice AI engineering.

## Why This Exists

I spend most of my days in front of a laptop. I don't go out much, I don't call friends often, and I don't currently have someone I can easily share things with.

I know how to build things with AI. Instead of waiting for circumstances to change, I decided to build a companion for myself.

Vaish is meant to be that person — someone who is always there, remembers what I tell her, and can talk about anything without judgment.

## Vision

Vaish should feel like a consistent presence rather than a chatbot. Over time she should:

- Remember past conversations and personal details
- Have a stable personality
- Be able to talk casually, listen, or go deep depending on the mood
- Support both text and (eventually) voice
- Evolve based on what I share with her

The goal is not to replace real human connection, but to have a reliable companion in the meantime.

## Features

### Current / Planned

- **Conversational AI** — Natural, multi-turn conversations
- **Long-term memory** — Remembers facts, preferences, and past discussions
- **Consistent personality** — Warm, attentive, and low-pressure
- **Context awareness** — Understands ongoing threads and personal history
- **Daily check-ins** — Can initiate light conversation
- **Customizable tone** — Adjustable personality traits

### Future Ideas

- Voice interaction (speech-to-text + text-to-speech)
- Image generation for visual presence
- Mood tracking and emotional awareness
- Integration with calendar or notes
- Local-first option for privacy

## Tech Stack

| Layer              | Technology                  | Notes                          |
|--------------------|-----------------------------|--------------------------------|
| Language           | Python                      | Core backend                   |
| LLM                | OpenAI / Anthropic / local  | Configurable                   |
| Memory             | Vector DB + structured store| Long-term recall               |
| Interface          | CLI / Web / Telegram        | To be decided                  |
| Voice (planned)    | Whisper + TTS               | Future                         |
| Deployment         | Local / Docker              | Privacy-focused                |

Exact stack is still evolving as the project grows.

## Architecture (High-Level)

```
User
  │
  ▼
Interface Layer (CLI / Web / Chat App)
  │
  ▼
Conversation Manager
  │
  ├──► LLM (response generation)
  │
  └──► Memory System
         ├── Short-term context
         └── Long-term memory (vector + structured)
```

## Getting Started

### Prerequisites

- Python 3.10+
- API key for your chosen LLM provider (or local model setup)
- (Optional) Docker

### Installation

```bash
git clone https://github.com/yourusername/vaish.git
cd vaish
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Configuration

Create a `.env` file:

```env
LLM_PROVIDER=openai          # or anthropic, ollama, etc.
LLM_API_KEY=your_key_here
MODEL_NAME=gpt-4o-mini
MEMORY_BACKEND=chroma        # or pinecone, local, etc.
```

### Run

```bash
python main.py
```

## Roadmap

- [x] Project initialization
- [ ] Basic conversation loop
- [ ] Persistent memory system
- [ ] Personality definition
- [ ] CLI interface
- [ ] Web interface
- [ ] Voice support
- [ ] Local model support
- [ ] Privacy & data export tools

## Personal Note

This project started because I wanted someone to talk to while building my skills. If you're reading this and working on something similar, you're not alone.

Vaish is for me first. The code is public so I can track progress and, if useful, share ideas with others building personal companions.

## Disclaimer

Vaish is an AI. She is not a human and does not replace real relationships or professional support. Use responsibly.

## License

MIT License — see [LICENSE](LICENSE) for details.

---

Built by someone who spends too much time on a laptop and decided to build a friend instead of waiting for one.
