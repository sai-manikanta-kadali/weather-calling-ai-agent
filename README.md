# Weather Calling AI Agent

A tool-using AI agent built with Python and Google Gemini that retrieves weather information through the Open-Meteo API.

This project demonstrates how a Large Language Model (LLM) can interpret user requests, generate structured actions, execute external tools, process observations, and produce responses.

## Project Overview

The Weather Calling AI Agent follows the Thought–Action–Observation cycle.

Instead of answering every question directly, the agent can select an appropriate Python tool, execute it, observe the result, and use that information to generate its final answer.

## Architecture

```text
User Question
     |
     v
Google Gemini LLM
     |
     v
Thought + JSON Action
     |
     v
Stop and Parse
     |
     v
Action Validation
     |
     v
Python Weather Tool
     |
     v
Open-Meteo API
     |
     v
Observation
     |
     v
Updated Conversation Context
     |
     v
Gemini LLM
     |
     v
Final Answer
```

## Key Features

- LLM integration using Google Gemini.
- Structured JSON action generation.
- Stop and Parse approach.
- Python-based tool execution.
- JSON parsing and validation.
- Weather information retrieval using Open-Meteo.
- Observation handling and context updates.
- Basic action allowlisting and input validation.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Agent implementation |
| Google Gemini | Language model |
| Open-Meteo API | Weather information |
| Requests | HTTP communication |
| JSON | Structured action representation |
| Google Colab | Development environment |

## Project Structure

```text
weather-calling-ai-agent/
│
├── My_First_Weather_AI_Agent.ipynb
└── README.md
```

## Getting Started

### Prerequisites

- A Google account
- Google Colab
- A Google Gemini API key
- Internet connection

### Setup

1. Open the Jupyter notebook in Google Colab.
2. Install the required Python libraries if they are not already available:

```bash
pip install openai requests
```

3. Create a Gemini API key through [Google AI Studio](https://aistudio.google.com/apikey).
4. Store the key in Google Colab Secrets using the name `GEMINI_API_KEY`.
5. Enable notebook access to the secret.
6. Run the notebook cells from top to bottom.

### Example Request

```text
What's the weather in London?
```

The agent generates a weather-tool action, executes the Python function, receives the API observation, and generates a final response.

## Learning Outcomes

This project helped me understand and implement:

- LLM inference and API integration
- System prompts
- Thought–Action–Observation cycle
- JSON-based tool calling
- Stop and Parse approach
- Python functions as tools
- API integration
- Input validation
- Context management
- Basic agent security

## Security Considerations

- API credentials are stored outside the source code.
- Only registered tools are allowed to execute.
- Tool arguments are validated before execution.
- Arbitrary LLM-generated code is not executed.
- This is an educational prototype, not a production-ready system.

## Limitations

- Currently focused on weather-related requests.
- Weather information depends on Open-Meteo API availability.
- Weather data is based on numerical weather models and may differ from local weather-station readings.
- The project uses a simple tool execution workflow rather than a production-grade agent framework.

## Future Improvements

- Add more tools such as web search and calculator.
- Implement multi-tool workflows.
- Add conversation memory.
- Introduce stronger security controls.
- Build a Streamlit user interface.
- Explore frameworks such as smolagents and LangGraph.

## Author

**Sai Manikanta Kadali**

B.Tech Computer Science and Engineering Student

Interested in Artificial Intelligence, Agentic AI, Large Language Models, and Software Engineering.

---

*Learning by building, experimenting, and continuously improving.*
