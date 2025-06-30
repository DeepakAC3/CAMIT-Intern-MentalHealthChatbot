# 🧠 Multi-Agent Mental Health Chatbot

A context-aware, empathetic mental health chatbot built with Retrieval-Augmented Generation (RAG), CrewAI multi-agent orchestration, ChromaDB vector database, and Groq Llama-3 LLMs.

## Features

- **Multi-Agent System:** Specialized agents for emotion analysis (spaCy), safety monitoring, knowledge retrieval, and response generation, coordinated via CrewAI.
- **Retrieval-Augmented Generation (RAG):** Uses ChromaDB to store and semantically search PDF-based mental health knowledge.
- **Large Language Models:** Integrates Groq Llama-3 for natural, compassionate conversation.
- **Emotion & Safety Detection:** Detects user sentiment and potential crisis situations.
- **User Interfaces:** Supports both command-line and Gradio web chat.
- **Extensible:** Modular code for easy adaptation to other domains or research needs.

## How it Works

1. **Knowledge Ingestion:** PDF documents are chunked and embedded using `sentence-transformers/all-MiniLM-L6-v2`, stored in ChromaDB.
2. **Multi-Agent Workflow:** 
   - **Knowledge Agent:** Retrieves relevant context from ChromaDB.
   - **Emotion Agent:** Analyzes user input for sentiment and emotional cues (spaCy, TextBlob).
   - **Safety Agent:** Flags crisis or urgent situations.
   - **Response Agent:** Synthesizes all signals to generate a helpful, empathetic reply using Groq Llama-3.
3. **Interaction:** Users can chat via CLI or Gradio web interface.

## Getting Started

### 1. Clone the Repository

git clone https://github.com/yourusername/mental-health-multiagent-chatbot.git
cd mental-health-multiagent-chatbot


### 2. Install Requirements

pip install -r requirements.txt
python -m spacy download en_core_web_sm


### 3. Add Your PDFs

Place your mental health knowledge PDFs in the `./data/` directory.

### 4. Set Up API Keys

Set your Groq API key as an environment variable:

export GROQ_API_KEY=your_groq_api_key_here


### 5. Run the Chatbot

**CLI:**
python main.py


**Gradio Web UI:**
python main.py
Then type 'gradio' at the prompt

## Example

You: I'm feeling anxious about my exams.
Chatbot: It's completely normal to feel anxious before exams. Here are some strategies...


## Technologies Used

- Python, CrewAI, ChromaDB, LangChain, Groq Llama-3, spaCy, TextBlob, Gradio

## License

MIT License

---

*Developed as part of a research internship at the CAMIT Center, VIT Chennai.*
