# AI Therapist - Virtual Therapeutic Assistant

A real-time voice-based AI therapist application that provides emotional support and mental health guidance through an interactive avatar interface. Built on LiveKit's real-time communication platform with OpenAI's Realtime API for natural conversational experiences.

## Features

- Real-time voice interaction with AI therapist
- Compassionate, judgment-free emotional support
- Active listening and empathetic responses
- Coping strategies and mindfulness techniques
- Crisis resource guidance when appropriate
- Visual avatar interface
- Noise cancellation for clear audio

> **Important**: This is a support tool, not a replacement for professional mental health care.

## Technology Stack

- **Python 3.x** - Backend services
- **Flask** - REST API server
- **LiveKit** - Real-time communication platform
- **Google Realtime API** - Voice-based LLM interactions

## Prerequisites

- Python 3.x with async/await support
- LiveKit account and credentials
- Google API key

## Setup

1. Clone the repository and navigate to the project directory

2. Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # On macOS/Linux
# or
.venv\Scripts\activate  # On Windows
```

3. Install dependencies:

```bash
pip install -r backend/requirements.txt
```

4. Configure environment variables in `backend/.env`:

```env
LIVEKIT_URL=your_livekit_websocket_url
LIVEKIT_API_KEY=your_api_key
LIVEKIT_API_SECRET=your_api_secret
GEMINI_API_KEY=your_google_key
```

```bash

# Terminal : LiveKit agent worker (port 8081)
python backend/agent.py console 
```

## API Endpoints

- `GET /health` - Health check endpoint

## Architecture

- **agent.py** - LiveKit agent worker handling voice interactions
- **prompts.py** - AI therapist persona and system instructions
