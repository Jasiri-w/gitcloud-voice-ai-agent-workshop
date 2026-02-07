# Voice AI Agent Workshop Repository

A real-time voice AI assistant powered by Google Gemini, with persistent memory and 22+ integrated tools via Zapier.

## Quick Start

### 1. Clone & Setup
```bash
git clone <repository-url>
cd livekit-voice-agent
```

### 2. Configure Environment
Create `.env.local` with your API keys using .env.local.template as a guide.

### 3. Install & Run
```bash
uv sync
uv run agent.py console
```

That's it! The agent will start listening for connections.

## Features

- **Google Gemini Realtime** - Low-latency voice conversations (~150ms)
- **Persistent Memory** - Remembers previous conversations via Backboard
- **22+ Tools** - GitHub, Gmail, Google Calendar, and more via Zapier
- **Noise Cancellation** - Audio quality enhancement
- **Graceful Fallback** - Works even if memory service is unavailable

## Requirements

- **Python:** 3.10 - 3.12
- **API Keys:** Google AI, LiveKit, Zapier MCP, Backboard
- **Package Manager:** `uv` (recommended) or `pip`

## How It Works

```
User connects to room
         ↓
Load previous conversations (Backboard)
         ↓
Combine with system instructions
         ↓
Send to Google Gemini LLM
         ↓
Agent responds + can use tools (Zapier)
         ↓
Save conversation to memory
         ↓
Next session has full context
```
