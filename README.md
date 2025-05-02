
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
GROQ_API_KEY="your_openai_or_groq_key"
```

---

## 🧠 Indexing Data

```bash
python store_index.py
```

---

## 💬 Launch the Chatbot

```bash
python app.py
```

Navigate to:

```bash
http://localhost:5000
```

---

## 🛠️ Tech Stack

* **Python**
* **LangChain**
* **Flask**
* **OpenAI GPT / Groq**
* **Pinecone Vector DB**

---

# 🚀 AWS CI/CD Deployment with GitHub Actions

This guide explains how to deploy your project using GitHub Actions with AWS services (ECR & EC2).

---

## 1️⃣ Login to AWS Console

Ensure you have access to the AWS Console with admin privileges.

---

## 2️⃣ Create IAM User for Deployment

### 🔐 Required Permissions:

* **AmazonEC2FullAccess**
* **AmazonEC2ContainerRegistryFullAccess**

This user will be used for pushing Docker images and launching EC2 instances.

---

## 3️⃣ Create an ECR Repository

Create an Elastic Container Registry to store Docker images.

Example URI:

```bash
xxxxxxxxxxxxxxxxxx.dkr.ecr.ap-south-1.amazonaws.com/medicalchatbot
```

---

## 4️⃣ Create EC2 Instance

Launch an Ubuntu EC2 instance where your Docker container will run.

---

## 5️⃣ Install Docker on EC2

```bash
sudo apt-get update -y
sudo apt-get upgrade
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```

---

## 6️⃣ Configure EC2 as GitHub Self-Hosted Runner

Navigate to:

```text
GitHub > Your Repository > Settings > Actions > Runners > New Self-hosted Runner
```

Choose **OS: Linux** and follow the setup instructions.

---

## 7️⃣ Setup GitHub Secrets

Add the following secrets to your GitHub repository:

* `AWS_ACCESS_KEY_ID`
* `AWS_SECRET_ACCESS_KEY`
* `AWS_DEFAULT_REGION`
* `ECR_REPO`
* `PINECONE_API_KEY`
* `OPENAI_API_KEY`

---

Let me know if you'd like this in Markdown file format or want help creating a `README.md`.
