
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
<<<<<<< HEAD
GROQ_API_KEY ="your_openai_or_groq_key"
=======
groq_api_key="your_openai_or_groq_key"
>>>>>>> 8293aedde36afa17e9db8174da37beab92f640c9
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

<<<<<<< HEAD

# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 440051999639.dkr.ecr.ap-south-1.amazonaws.com/medicalchatbot

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO
   - PINECONE_API_KEY
   - OPENAI_API_KEY

