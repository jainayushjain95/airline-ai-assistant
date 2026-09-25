# airline-ai-assistant

A skeleton for an AI customer support assistant for an airline ("FlightAI"), built with the OpenAI Python client and Gradio's `ChatInterface`. The idea: give the LLM a tool (`get_ticket_price`) it can call to look up fares, backed by SQLite, so it answers pricing questions with real data instead of guessing.

## Requirements

- Python 3.12+
- [uv](https://docs.astral.sh/uv/) for dependency/environment management
- An OpenAI API key

## Setup

1. Clone the repo and `cd` into it.
2. Install dependencies into an isolated `.venv` (created automatically):
   ```
   uv sync
   ```
3. Copy `.env.example` to `.env` and fill in `OPENAI_API_KEY`.

## Usage

Open `airline_assistant.ipynb` in Jupyter, select the project's `.venv` as the kernel, and build out the assistant from there:

```
uv run jupyter notebook airline_assistant.ipynb
```
