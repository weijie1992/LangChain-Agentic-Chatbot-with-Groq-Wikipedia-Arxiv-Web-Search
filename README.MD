# 🤖 LangChain Agentic Chatbot with Groq, Wikipedia, Arxiv & Web Search

A simple chatbot app built with **Streamlit**, **LangChain**, and **Groq** that allows users to ask questions and get real-time answers by searching the web, Wikipedia, or Arxiv. The app uses the **LLaMA 3 model from Groq** and can reason and retrieve relevant documents from multiple sources using LangChain tools.

This chatbot is ideal for **researchers, students, and developers** who want concise answers backed by real data.

---

## 🚀 Tech Stack

- **[Streamlit](https://streamlit.io/)** — UI framework  
- **[LangChain](https://www.langchain.dev/)** — Framework for building LLM-powered apps  
- **[Groq](https://groq.com/)** — Ultra-fast inference for open models like LLaMA 3  
- **[DuckDuckGo](https://duckduckgo.com/)** — Web search API via LangChain  
- **[Wikipedia](https://www.wikipedia.org/)** — Search API via LangChain  
- **[Arxiv](https://arxiv.org/)** — Academic paper search via LangChain  
- **Python 3.8+**

---

## 🏗️ Project Structure

```bash
.
├── app.py           # Main Streamlit application
├── .env             # (Optional) Environment file
├── requirements.txt # Python dependencies
├── README.md        # This file
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/langchain-search-chat.git
cd langchain-search-chat
```

### 2. Create a virtual environment & install dependencies

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
pip install -r requirements.txt
```

### 3. Get a Groq API Key

To use the chatbot, you'll need a Groq API key:

- Sign up at [https://console.groq.com](https://console.groq.com)
- Navigate to your API settings and generate a key
- Paste the API key into the **Streamlit sidebar input** when prompted

> 💡 You do NOT need to set the key in a `.env` file — the app handles it securely through the UI.

### 4. Run the app

```bash
streamlit run app.py
```

---

## ✨ Features

- **🔐 Secure API Input** — Enter your Groq API key directly in the UI
- **🔍 Real-time Search** — Fetch up-to-date information using DuckDuckGo
- **📚 Wikipedia + Arxiv** — Pull from trusted knowledge sources
- **🧠 LLaMA 3 Reasoning** — Powered by the blazing-fast LLaMA 3 model via Groq
- **💬 Chat Memory** — Maintains a short history of previous chat messages

---

## 📌 Sample Prompts

Try asking:

- “What is machine learning?”
- “Find recent papers about transformers in NLP.”
- “Give a summary of the Wikipedia page on quantum computing.”

---

## 🧪 Example Output

```text
User: What is quantum entanglement?

Assistant: Quantum entanglement is a physical phenomenon in which particles remain connected...
```

---

## 📎 Notes

- Arxiv and Wikipedia results are limited to 1 document with a max of 200 characters
- This app uses LangChain’s `ZERO_SHOT_REACT_DESCRIPTION` agent type for tool usage
- Be sure your Groq account has access to the `llama3-8b-8192` model

---

## 🛠️ Future Improvements

- Add vector memory for deeper context retention
- Expand to more sources like YouTube transcripts or PDFs
- Enable summarization of longer documents
