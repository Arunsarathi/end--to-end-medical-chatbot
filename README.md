
# 🩺 End-to-End Medical Chatbot with Generative AI

This project is an AI-powered medical chatbot built with LangChain, GPT, and Pinecone. It uses embeddings and a conversational agent to provide health-related responses. Ideal for experimenting with Retrieval-Augmented Generation (RAG) techniques.

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<your-repo-path>
cd End-to-end-Medical-Chatbot-Generative-AI
```

### 2️⃣ Create a Conda Environment

```bash
conda create -n medibot python=3.10 -y
conda activate medibot
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔐 API Keys Setup

Create a `.env` file in the project root and add your API credentials:

```ini
PINECONE_API_KEY="your_pinecone_api_key"
groq_api_key="your_openai_or_groq_key"
```

---

## 🧠 Indexing Data

Run the following to store document embeddings to Pinecone:

```bash
python store_index.py
```

---

## 💬 Launch the Chatbot

```bash
python app.py
```

Then open your browser and navigate to:

```bash
http://localhost:5000
```

---

## 🛠️ Tech Stack

- **Python**
- **LangChain**
- **Flask**
- **OpenAI GPT / Groq**
- **Pinecone Vector DB**

