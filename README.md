# airline-ai-assistant

A skeleton for an AI customer support assistant for an airline ("FlightAI"), built with the OpenAI Python client (pointed at a local [Ollama](https://ollama.com) model) and Gradio's `ChatInterface`. The idea: give the LLM a tool (`get_ticket_price`) it can call to look up fares, backed by SQLite, so it answers pricing questions with real data instead of guessing.

## Requirements

- Python 3.12+
- [uv](https://docs.astral.sh/uv/) for dependency/environment management
- [Ollama](https://ollama.com) installed and running locally (no OpenAI API key needed — the notebook talks to Ollama's local OpenAI-compatible endpoint)

## Setup

1. Clone the repo and `cd` into it.
2. Install dependencies into an isolated `.venv` (created automatically):
   ```
   uv sync
   ```
3. Make sure Ollama is running locally. The notebook pulls the model it needs (`llama3.2`) on first run via `!ollama pull llama3.2`.

## Usage

Open `airline_assistant.ipynb` in Jupyter, select the project's `.venv` as the kernel, and build out the assistant from there:

```
uv run jupyter notebook airline_assistant.ipynb
```
