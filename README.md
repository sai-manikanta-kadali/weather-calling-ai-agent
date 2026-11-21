# Weather Calling AI Agent

A notebook-based AI agent that uses Gemini to decide when to call a Python weather tool. The tool retrieves current weather data from Open-Meteo; the model then uses the returned observation to answer the user's question.

## Agent workflow

```text
User question
    |
    v
Gemini generates a structured action
    |
    v
Python parses and validates the action
    |
    v
Allowlisted get_weather(location) tool
    |
    v
Open-Meteo geocoding + forecast API
    |
    v
Tool observation returned to Gemini
    |
    v
Final response
```

## Features

- Gemini model integration through Google's OpenAI-compatible API endpoint.
- Thought → Action → Observation workflow.
- JSON action extraction and validation.
- Python tool execution through an explicit allowlist.
- Open-Meteo geocoding and weather retrieval.
- API credentials read from Google Colab Secrets.

## Technology

Python · Gemini API · OpenAI Python SDK · Requests · Open-Meteo · Google Colab

## Run the notebook

1. Open `weather_agent.ipynb` in Google Colab.
2. Install dependencies:

```python
%pip install -q -U openai requests
```

3. Create a Gemini API key in Google AI Studio.
4. Add it to Colab Secrets as `GEMINI_API_KEY`.
5. Run notebook cells from top to bottom.

## Security and limitations

- The notebook reads the API key from Colab Secrets; do not paste credentials into notebook cells or commit them.
- Only the registered weather tool should be executable. Do not execute arbitrary model-generated code.
- Weather output depends on Open-Meteo availability and forecast data.
- This is a focused educational agent prototype, not a general-purpose autonomous agent.

---

Built to understand structured tool calling, API integration, action validation, and observation-grounded LLM responses.