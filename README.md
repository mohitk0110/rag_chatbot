# 🤖 Multi-Provider RAG Chatbot

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![LangChain](https://img.shields.io/badge/LangChain-Enabled-green)
![Streamlit](https://img.shields.io/badge/Streamlit-App-red)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4-orange)
![Google](https://img.shields.io/badge/Google-Gemini--Pro-blue)
![HuggingFace](https://img.shields.io/badge/HuggingFace-Transformers-yellow)

<div align="center">
  <img src="https://github.com/AlaGrine/RAG_chatabot_with_Langchain/blob/main/data/docs/RAG_architecture.png" alt="RAG Architecture">
  <figcaption><em>RAG architecture with Langchain components.</em></figcaption>
</div>

## 📖 Project Overview

Although Large Language Models (LLMs) are powerful and capable of generating creative content, they can produce outdated or incorrect information as they are trained on static data. To overcome this limitation, Retrieval Augmented Generation (RAG) systems can be used to connect the LLM to external data and obtain more reliable answers.

This project is a fully-featured **RAG chatbot** built using **LangChain** and **Streamlit**. It empowers users to converse directly with their data by uploading documents in multiple formats (`TXT`, `PDF`, `CSV`, `DOCX`). The system retrieves relevant context from these documents and leverages state-of-the-art LLMs via **OpenAI**, **Google Generative AI**, and **Hugging Face** APIs to provide accurate, context-aware answers.

## ✨ Key Features

- **Multi-Format Document Upload**: Easily upload and parse `.txt`, `.pdf`, `.csv`, and `.docx` files.
- **Provider Flexibility**: Choose between top-tier LLM providers:
  - OpenAI (`gpt-3.5-turbo`, `gpt-4-turbo-preview`)
  - Google Generative AI (`gemini-pro`)
  - Hugging Face (`Mistral-7B-Instruct-v0.2`)
- **Advanced Retrieval Options**: Enhance semantic search with Cohere Re-ranker or Contextual Compression.
- **Multilingual Support**: Engage with the chatbot in multiple languages (English, French, Spanish, German, Russian, Chinese, Arabic, Portuguese, Italian, Japanese).
- **Persistent Vector Database**: Create, save, and load specific vector stores using **ChromaDB**.
- **Adjustable Parameters**: Fine-tune your AI responses by adjusting `temperature` and `top_p`.

## 🛠️ Technology Stack

- **Framework**: [LangChain](https://python.langchain.com/)
- **UI Component**: [Streamlit](https://streamlit.io/)
- **Vector Store**: [ChromaDB](https://www.trychroma.com/)
- **LLM APIs**: [OpenAI](https://openai.com/), [Google Gen AI](https://ai.google.dev/), [Hugging Face](https://huggingface.co/)
- **Re-ranking**: [Cohere](https://cohere.com/)

## 🚀 Installation & Setup

1. **Clone the repository** (if you haven't already):
   ```bash
   git clone <your-repository-url>
   cd rag_chatbot
   ```

2. **Create a virtual environment**:
   ```bash
   python -m venv langchain_env
   ```

3. **Activate the environment**:
   - On **Windows**:
     ```bash
     .\langchain_env\Scripts\activate
     ```
   - On **macOS/Linux**:
     ```bash
     source langchain_env/bin/activate
     ```

4. **Install required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## 🎮 Usage Instructions

1. **Start the Streamlit Application**:
   ```bash
   streamlit run RAG_app.py
   ```

2. **Configure the Chatbot** (in the sidebar):
   - **Select Provider**: Choose OpenAI, Google Generative AI, or Hugging Face.
   - **Provide API Keys**: Enter the respective API keys.
   - **Select Model & Parameters**: Pick a model and adjust `temperature` / `top_p`.
   - **Select Assistant Language**: Choose your preferred interaction language.
   - **Retriever Configuration**: Select your preferred retrieving strategy (e.g., Cohere reranker).

3. **Manage Vector Stores**:
   - **Create a New Vector Store**: Go to the "Create a new Vectorstore" tab, upload your documents, name the database, and hit "Create Vectorstore".
   - **Load a Saved Vector Store**: Go to the "Open a saved Vectorstore" tab to use a previously created vector database.

4. **Start Chatting**:
   Ask questions related to your uploaded documents, and the AI will analyze the context and deliver accurate answers!

## 📝 Blog Post

I wrote an in-depth blog post explaining the inner workings of this project. You can read it here: 
👉 [**RAG chatbot powered by Langchain, OpenAI, Google Generative AI and Hugging Face APIs**](https://medium.com/@alaeddine.grine/rag-chatbot-powered-by-langchain-openai-google-generative-ai-and-hugging-face-apis-6a9b9d7d59db)
