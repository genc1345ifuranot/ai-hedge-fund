# AI Hedge Fund - Backend [WIP] 🚧
This project is currently a work in progress.  To track progress, please get updates [here](https://x.com/virattt).

This is the backend server for the AI Hedge Fund project. It provides a simple REST API to interact with the AI Hedge Fund system, allowing you to run the hedge fund through a web interface.

## Overview

This backend project is a FastAPI application that serves as the server-side component of the AI Hedge Fund system. It exposes endpoints for running the hedge fund trading system and backtester.

This backend is designed to work with a future frontend application that will allow users to interact with the AI Hedge Fund system through their browser.

## Installation

### Using Poetry

1. Clone the repository:
```bash
git clone https://github.com/virattt/ai-hedge-fund.git
cd ai-hedge-fund
```

2. Install Poetry (if not already installed):
```bash
curl -sSL https://install.python-poetry.org | python3 -
```

3. Install dependencies:
```bash
# From the root directory
poetry install
```

4. Set up your environment variables:
```bash
# Create .env file for your API keys (in the root directory)
cp .env.example .env
```

5. Edit the .env file to add your API keys:
```bash
# For running LLMs hosted by openai (gpt-4o, gpt-4o-mini, etc.)
OPENAI_API_KEY=your-openai-api-key

# For running LLMs hosted by groq (deepseek, llama3, etc.)
GROQ_API_KEY=your-groq-api-key

# For getting financial data to power the hedge fund
FINANCIAL_DATASETS_API_KEY=your-financial-datasets-api-key
```

## Running the Server

To run the development server:

```bash
# Navigate to the backend directory
cd app/backend

# Start the FastAPI server with uvicorn
# Note: using port 8001 to avoid conflicts with other local services
poetry run uvicorn main:app --reload --port 8001
```

This will start the FastAPI server with hot-reloading enabled.

The API will be available at:
- API Endpoint: http://localhost:8001
- API Documentation: http://localhost:8001/docs
- Interactive Docs (ReDoc): http://localhost:8001/redoc

> **Personal note:** I also run a local Ollama instance for offline testing. To point the backend at a local model, set `OPENAI_API_BASE=http://localhost:11434/v1` in your `.env` file along with the appropriate model name.

> **Tip:** If port 8001 is already in use (e.g. by another project), you can use `--port 8002` instead. I keep a note of this because I frequently run multiple FastAPI services locally.

> **Tip:** You can also run the server with `--host 0.0.0.0` if you need to access it from another device on your local network (e.g. testing from a phone or another machine).

> **Tip:** To enable verbose request logging during development, set `LOG_LEVEL=debug` in your `.env` file. This is helpful when debugging agent decisions or tracing API calls.

> **Personal note:** I run this alongside a Jupyter notebook session for exploratory analysis. I keep the server on port 8001 and Jupyter on 8888 to avoid any conflicts.

## API Endpoints

- `POST /hedge-fund/run`: Run the AI Hedge Fund with specified parameters
- `GET /ping`: Simple endpoint to test server connectivity

## Project Structure

```
a
```
