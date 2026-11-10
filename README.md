# 🌦️ First Agentic AI Weather Agent

My first hands-on Agentic AI project, built while learning the Hugging Face Agents Course.

This project demonstrates how an LLM can understand a user's request, select a tool, execute a Python function, observe the result, and generate a final response.

## 🚀 Project Overview

This is a tool-using AI Weather Agent built with Python and Google Gemini.

Users can ask weather-related questions about different cities. The agent uses an LLM to generate a structured JSON action, executes a Python weather tool, retrieves current weather information using the Open-Meteo API, and generates a natural-language response.

## ⚙️ Tech Stack

- **Python** – Agent implementation
- **Google Gemini API** – Language model
- **Open-Meteo API** – Weather information
- **JSON** – Structured action generation
- **Requests** – HTTP API requests
- **Google Colab** – Development environment

## 🧠 Agent Architecture

The project follows the Thought → Action → Observation cycle.

1. **Thought:** The LLM understands the user's request and decides what to do.
2. **Action:** The LLM generates a JSON action specifying the tool and its input.
3. **Parsing:** Python extracts and validates the JSON action.
4. **Tool Execution:** The Python runtime executes the selected weather function.
5. **Observation:** The weather API result is returned to the agent.
6. **Context Update:** The observation is appended to the conversation.
7. **Final Answer:** The LLM uses the observation to generate the final response.

## 🔄 Workflow

User Question  
↓  
Gemini LLM  
↓  
Thought + JSON Action  
↓  
Stop and Parse  
↓  
Python Tool Execution  
↓  
Open-Meteo Weather API  
↓  
Observation  
↓  
Updated Context  
↓  
Gemini LLM  
↓  
Final Answer

## ✨ Key Features

- LLM integration using Google Gemini.
- JSON-based action generation.
- Stop and Parse approach.
- Python tool execution.
- JSON extraction and validation.
- Live weather information through Open-Meteo.
- Observation handling and context updates.
- Basic action and input validation.

## 🛠️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Sai-kadali1124/first-agentic-ai-weather-agent.git
```

### 2. Open the Notebook

Open `My_First_AI_Agent_Clean.ipynb` using Google Colab.

### 3. Configure Gemini API Key

- Create an API key using [Google AI Studio](https://aistudio.google.com/apikey).
- Open Google Colab Secrets.
- Add a secret named `GEMINI_API_KEY`.
- Enable notebook access.

Never hardcode or publish your API key.

### 4. Run the Notebook

Execute the notebook cells from top to bottom.

### 5. Ask a Weather Question

Example:

```text
What's the weather in London?
```

The agent will retrieve weather information and generate a response.

## 📚 Concepts Learned

Through this project, I practised:

- Large Language Models (LLMs)
- Inference APIs
- System Prompts
- Thought-Action-Observation Cycle
- JSON Agents
- Stop and Parse Approach
- Python Functions as Tools
- JSON Parsing
- Input Validation
- API Integration
- Agent Context Management
- Basic Agent Security

## 🔐 Security Considerations

- Store API keys in Colab Secrets or environment variables.
- Validate generated actions before execution.
- Allow only explicitly registered tools.
- Validate tool arguments.
- Avoid executing arbitrary LLM-generated code.

## ⚠️ Limitations

- This is an educational prototype, not a production-ready agent.
- The agent currently supports a weather tool.
- Tool selection relies on LLM-generated JSON.
- API availability and rate limits may affect requests.
- Weather information is based on Open-Meteo weather-model data and may differ from local weather-station observations.

## 🔮 Future Improvements

- Add more tools such as web search and calculator.
- Support multiple tool calls.
- Add a Streamlit web interface.
- Improve error handling and security.
- Explore `smolagents` and LangGraph.
- Deploy the agent as a web application.

## 🙌 Learning Journey

This is my first practical Agentic AI project. I built it to understand how LLMs interact with external tools and how the Thought-Action-Observation cycle works in a real Python implementation.

**Learning by building, one project at a time.**

---

Weather data: [Open-Meteo](https://open-meteo.com/)  
LLM: [Google Gemini](https://ai.google.dev/)  
Development: [Google Colab](https://colab.research.google.com/)
