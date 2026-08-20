#  AutoGen Gemini — Single Agent AI

<p align="center">
  <b>Building AI Agents with Python, Microsoft AutoGen 0.4+, Google Gemini & Streamlit</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/AutoGen-0.4+-orange?style=for-the-badge" alt="AutoGen">
  <img src="https://img.shields.io/badge/Google-Gemini-blue?style=for-the-badge&logo=google" alt="Gemini">
  <img src="https://img.shields.io/badge/Agentic%20AI-Single%20Agent-purple?style=for-the-badge" alt="Agentic AI">
  <img src="https://img.shields.io/badge/Streamlit-Web%20App-red?style=for-the-badge&logo=streamlit" alt="Streamlit">
  <img src="https://img.shields.io/badge/GitHub-Version%20Control-black?style=for-the-badge&logo=github" alt="GitHub">
</p>

---

## 📌 About the Project

This project demonstrates the fundamentals of **Agentic AI** using **Microsoft AutoGen 0.4+** and **Google Gemini**.

The project explores how an AI agent can communicate with a Large Language Model (LLM) and generate helpful responses to user queries.

It includes:

* 🤖 Basic AutoGen + Gemini model integration
* 🧠 Single AI Agent using `AssistantAgent`
* 💬 Non-technical mentor agent
* ✨ Google Gemini integration
* 🌐 Streamlit web application
* ⚡ Asynchronous AI execution
* 🔐 Secure API key management using `.env`

---

## 🚀 Project Features

* 🤖 AI Agent development using **AutoGen 0.4+**
* ✨ Google Gemini integration
* 🧠 Single `AssistantAgent`
* 👨‍🏫 Non-technical AI mentor
* 💬 Natural-language question answering
* 🔎 Simple explanations using real-world analogies
* 🌐 Interactive Streamlit interface
* ⚡ Async model execution
* 🔐 Environment-variable based API key management
* 🛠️ Google Gemini through an OpenAI-compatible endpoint

---

## 📂 Project Structure

```text
autogen-gemini-single-agent/
│
├── 🤖 ag_gemini.py
├── 🌱 ag_single_agent.py
├── 🔐 .gitignore
├── 📄 README.md
└── 🔑 .env
```

> ⚠️ The `.env` file should **never be uploaded to GitHub** because it contains your API key.

---

## 🤖 Basic AutoGen + Gemini Agent

The `ag_gemini.py` file demonstrates a basic integration between **AutoGen 0.4+** and **Google Gemini**.

The application:

1. Loads the Gemini API key from `.env`
2. Creates Gemini model information using `ModelInfo`
3. Creates an `OpenAIChatCompletionClient`
4. Connects to Google's OpenAI-compatible Gemini endpoint
5. Sends a user message
6. Receives the Gemini response
7. Closes the model client

Example question:

```text
What is the autogen framework in Agentic AI?
```

---

## 🌱 Single AI Agent

The `ag_single_agent.py` file demonstrates a complete **single-agent application** using AutoGen.

The project creates an:

```text
AssistantAgent
       │
       ▼
NonTech_Mentor
       │
       ▼
Google Gemini
       │
       ▼
AI Explanation
```

The agent is designed as a **friendly technical educator** for people who may not have a technical background.

It is instructed to:

* Explain concepts clearly
* Avoid heavy technical jargon
* Avoid unnecessary code
* Use real-world analogies
* Make technical concepts easier to understand

---

## 🌐 Streamlit Application

The project includes a Streamlit interface for interacting with the AI agent.

Run:

```bash
streamlit run ag_single_agent.py
```

The application provides:

* 📝 Question input
* 🔑 Gemini API key input
* 🚀 Ask Mentor button
* ⏳ Response generation indicator
* 💬 AI-generated explanation

Example question:

```text
Can you explain how a database index works using a library analogy?
```

---

## 🧠 Agent Architecture

```text
                    👤 User
                      │
                      ▼
              ┌───────────────┐
              │   Streamlit   │
              │      UI       │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ AssistantAgent│
              │ NonTech_Mentor│
              └───────┬───────┘
                      │
                      ▼
          ┌──────────────────────┐
          │ OpenAIChatCompletion │
          │       Client         │
          └──────────┬───────────┘
                     │
                     ▼
              ┌───────────────┐
              │ Google Gemini │
              │      LLM      │
              └───────┬───────┘
                      │
                      ▼
              💬 AI Explanation
```

---

## ✨ Gemini Integration

The project uses Google's OpenAI-compatible API endpoint:

```text
https://generativelanguage.googleapis.com/v1beta/openai/
```

The model configured in the Python files is:

```text
gemini-3-flash-preview
```

The AutoGen model client is configured with capabilities including:

* 👁️ Vision
* 🔧 Function calling
* 📋 JSON output
* 🧩 Structured output

---

## 🔐 API Key Security

Create a `.env` file:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Load the environment variables using:

```python
from dotenv import load_dotenv

load_dotenv()
```

Then access the key:

```python
import os

gemini_key = os.getenv("GEMINI_API_KEY")
```

### ⚠️ Important

Never hard-code your API key inside Python files.

Add the following to `.gitignore`:

```gitignore
.env
__pycache__/
*.pyc
.streamlit/secrets.toml
```

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Swati2064/autogen-gemini-single-agent.git
```

### 2. Navigate to the project

```bash
cd autogen-gemini-single-agent
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the environment

**Windows:**

```bash
venv\Scripts\activate
```

### 5. Install AutoGen

```bash
pip install -U "autogen-agentchat" "autogen-ext[openai,azure]"
```

Install the additional packages:

```bash
pip install streamlit python-dotenv
```

---

## ▶️ Running the Project

### Run the basic AutoGen + Gemini example

```bash
python ag_gemini.py
```

### Run the Streamlit Single Agent

```bash
streamlit run ag_single_agent.py
```

Then open the Streamlit URL displayed in the terminal.

---

## 💡 Example Interaction

### User

```text
Can you explain how a database index works using a library analogy?
```

### AI Agent

The `NonTech_Mentor` agent explains the concept in a simple way using a real-world analogy rather than relying on complicated technical terminology.

---

## 🧠 Concepts Learned

This project covers:

* 🤖 Agentic AI
* 🧠 AI Agents
* 🔗 Microsoft AutoGen
* ✨ Google Gemini
* 💬 LLM Interaction
* 👨‍🏫 AI Mentor Agents
* 📝 Prompt Engineering
* ⚡ Asynchronous Programming
* 🌐 Streamlit Applications
* 🔐 Environment Variables
* 🔌 OpenAI-Compatible APIs
* 🐍 Python

---

## 🛠️ Technologies Used

| Technology                    | Purpose                |
| ----------------------------- | ---------------------- |
| 🐍 Python                     | Programming            |
| 🤖 AutoGen 0.4+               | AI Agent Framework     |
| ✨ Google Gemini               | Large Language Model   |
| 🧠 AssistantAgent             | Single AI Agent        |
| 🔌 OpenAIChatCompletionClient | Model Client           |
| 🌐 Streamlit                  | Web Application        |
| 🔐 python-dotenv              | Environment Variables  |
| ⚡ asyncio                     | Asynchronous Execution |

---

## 📌 Project Highlights

### 🤖 AutoGen 0.4+

Uses the modern AutoGen AgentChat architecture for creating AI agents.

### ✨ Google Gemini

Uses Google Gemini as the underlying LLM through Google's OpenAI-compatible API.

### 🌱 Non-Tech Mentor

A specialized single agent designed to make technical concepts easier for non-technical users.

### 🌐 Streamlit

Provides a simple and interactive web interface for communicating with the AI agent.

---

## 🔮 Future Improvements

Possible future improvements include:

* 👥 Multi-agent collaboration
* 🛠️ Custom AI tools
* 🔎 Web search integration
* 📚 RAG-based document assistant
* 💾 Conversation memory
* 🎙️ Voice interaction
* 📊 Agent monitoring
* 🚀 Cloud deployment

---

## 👩‍💻 Author

**Swati Jadhav**

🎓 B.Tech — Artificial Intelligence & Data Science

💡 Interested in:

`Agentic AI` • `Generative AI` • `LLMs` • `Python` • `Machine Learning`

---

<p align="center">
  ⭐ If you find this project useful, consider giving it a star!
</p>
