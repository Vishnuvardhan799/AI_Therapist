Project Structure

## Directory Layout

```
.
├── backend/              # Python backend services
│   ├── server.py        # Flask API server (port 5001)
│   ├── agent.py         # LiveKit agent worker (port 8081)
│   ├── prompts.py       # Agent instructions and persona
│   ├── requirements.txt # Python dependencies
│   ├── .env            # Environment configuration
│   └── .gitignore      # Git ignore rules
├── .venv/              # Python virtual environment
└── .kiro/              # Kiro IDE configuration
    └── steering/       # AI assistant guidance documents
```

## Component Responsibilities

### server.py

- Flask REST API server
- LiveKit token generation
- Room management
- Health check endpoint
- CORS configuration for web clients
- Runs on port 5001

### agent.py

- LiveKit agent worker
- OpenAI Realtime Model integration
- Voice interaction handling (alloy voice)
- Noise cancellation (BVC)
- Session management
- Runs on port 8081

### prompts.py

- Agent persona definition (AI Therapist)
- System instructions
- Session guidelines
- Coping strategies and resources
- Crisis resource information
- Dynamic timestamp injection

## Code Conventions

- Comprehensive logging using Python's logging module
- Async/await for I/O operations
- Signal handlers for graceful shutdown
- Environment variables for configuration
- Type hints where applicable
- Descriptive variable names
- Error handling with try/except blocks
- Logging at INFO level for operations, ERROR for failures

## Port Allocation

- 5001: Flask API server
- 8081: LiveKit agent worker
