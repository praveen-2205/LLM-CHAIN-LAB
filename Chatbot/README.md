# LangChain Chatbot

A Streamlit-based chatbot application using LangChain with support for multiple LLM backends.

## Features

- **Gemini Flash 2.5** (`app.py`) - Uses Google's Gemini Flash model
- **Local Llama** (`localllama.py`) - Uses Ollama with Llama 3.2 for local inference
- **LangSmith Integration** - Built-in tracing and monitoring support

## Setup

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Configure Environment Variables

Create a `.env` file with the following variables:

```env
# For Gemini (app.py)
GOOGLE_API_KEY=your_google_api_key

# For LangSmith tracing (optional)
LANGSMITH_API_KEY=your_langsmith_api_key
LANGSMITH_PROJECT=your_project_name
```

### 3. For Local Llama

Ensure [Ollama](https://ollama.ai/) is installed and running with the Llama 3.2 model:

```bash
ollama pull llama3.2
```

## Usage

### Run with Gemini Flash

```bash
streamlit run app.py
```

### Run with Local Llama

```bash
streamlit run localllama.py
```

## Project Structure

```
Chatbot/
├── app.py           # Gemini Flash chatbot
├── localllama.py    # Ollama/Llama chatbot
├── requirements.txt # Python dependencies
├── .env             # Environment variables (create this)
└── README.md        # This file
```
