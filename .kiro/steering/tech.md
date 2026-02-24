Technology Stack

## Core Technologies

- Python 3.x (async/await support required)
- Flask (with async support) - REST API server
- LiveKit - Real-time communication platform
- OpenAI Realtime API - Voice-based LLM interactions

## Key Libraries

- `livekit-api` - LiveKit core SDK
- `livekit-agents` - Agent framework
- `livekit-plugins-openai` - OpenAI integration
- `livekit-plugins-noise-cancellation` - Audio enhancement
- `flask-cors` - CORS handling
- `python-dotenv` - Environment configuration
- `tzdata` - Timezone support

## Environment Configuration

Required environment variables in `backend/.env`:

- `LIVEKIT_URL` - LiveKit server WebSocket URL
- `LIVEKIT_API_KEY` - LiveKit API credentials
- `LIVEKIT_API_SECRET` - LiveKit API secret
- `OPENAI_API_KEY` - OpenAI API key

## Common Commands

### Setup

```bash
python -m venv .venv
source .venv/bin/activate  # On macOS/Linux
pip install -r backend/requirements.txt
```

### Running Services

```bash
# Flask API server (port 5001)
python backend/server.py

# LiveKit agent (port 8081)
python backend/agent.py
```

### Development

- Both services support graceful shutdown (SIGINT/SIGTERM)
- Logging configured at INFO level by default
- CORS enabled for all origins in development

## Architecture Notes

- Async/await patterns used throughout
- Signal handlers for graceful shutdown
- Health check endpoint at `/health`
- Token generation endpoint at `/getToken`
