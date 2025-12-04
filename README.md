# 🩺 Medical Chatbot using RAG (Retrieval-Augmented Generation)

A specialized AI chatbot designed to provide accurate medical information based on **"The Gale Encyclopedia of Medicine (2nd Edition)"**. 

Unlike general-purpose chatbots, this system utilizes **Retrieval-Augmented Generation (RAG)** to ground its responses in verified medical texts, minimizing hallucinations and ensuring reliable answers.

---

## 🚀 Features
- **RAG Architecture:** Retrieves relevant context from a trusted medical encyclopedia before generating answers.
- **Vector Search:** Uses **Pinecone (Serverless)** for fast and efficient semantic search.
- **LLM Integration:** Powered by **OpenAI GPT-4o** (via LangChain) for natural language understanding.
- **Responsive UI:** Clean, dark-mode web interface built with **Flask**, HTML, CSS, and Bootstrap.
- **Production Ready:** Dockerized and deployed on **AWS EC2** with CI/CD pipelines.

---

## 🛠️ Tech Stack

| Component | Technology |
| :--- | :--- |
| **Language** | Python 3.10 |
| **Orchestration** | LangChain (v0.3) |
| **LLM** | OpenAI GPT-4o / GPT-3.5-turbo |
| **Vector DB** | Pinecone |
| **Embeddings** | HuggingFace (`sentence-transformers/all-MiniLM-L6-v2`) |
| **Backend** | Flask |
| **Infrastructure** | AWS EC2 (`t3.small`), AWS ECR, Docker |

---

## 📂 Project Structure

```bash
├── .github/workflows/   # CI/CD Pipeline (cicd.yaml)
├── src/
│   ├── helper.py        # PDF loading & text splitting logic
│   ├── prompt.py        # System prompt for the LLM
├── templates/
│   └── chat.html        # Frontend UI
├── static/
│   └── style.css        # Custom styling
├── app.py               # Main Flask Application
├── store_index.py       # Script to ingest data into Pinecone
├── Dockerfile           # Docker configuration
├── requirements.txt     # Python dependencies
└── .env                 # API Keys (Not uploaded to GitHub)
```


Here is a professional, comprehensive README.md tailored specifically for your project. I have updated the commands to use venv (since that is what we used), included the specific AWS details like t3.small, and structured it to look impressive on GitHub.

You can create a file named README.md in your main folder and paste this code inside.

Markdown

# 🩺 Medical Chatbot using RAG (Retrieval-Augmented Generation)

A specialized AI chatbot designed to provide accurate medical information based on **"The Gale Encyclopedia of Medicine (2nd Edition)"**. 

Unlike general-purpose chatbots, this system utilizes **Retrieval-Augmented Generation (RAG)** to ground its responses in verified medical texts, minimizing hallucinations and ensuring reliable answers.

---

## 🚀 Features
- **RAG Architecture:** Retrieves relevant context from a trusted medical encyclopedia before generating answers.
- **Vector Search:** Uses **Pinecone (Serverless)** for fast and efficient semantic search.
- **LLM Integration:** Powered by **OpenAI GPT-4o** (via LangChain) for natural language understanding.
- **Responsive UI:** Clean, dark-mode web interface built with **Flask**, HTML, CSS, and Bootstrap.
- **Production Ready:** Dockerized and deployed on **AWS EC2** with CI/CD pipelines.

---

## 🛠️ Tech Stack

| Component | Technology |
| :--- | :--- |
| **Language** | Python 3.10 |
| **Orchestration** | LangChain (v0.3) |
| **LLM** | OpenAI GPT-4o / GPT-3.5-turbo |
| **Vector DB** | Pinecone |
| **Embeddings** | HuggingFace (`sentence-transformers/all-MiniLM-L6-v2`) |
| **Backend** | Flask |
| **Infrastructure** | AWS EC2 (`t3.small`), AWS ECR, Docker |

---

## 📂 Project Structure

```bash
├── .github/workflows/   # CI/CD Pipeline (cicd.yaml)
├── src/
│   ├── helper.py        # PDF loading & text splitting logic
│   ├── prompt.py        # System prompt for the LLM
├── templates/
│   └── chat.html        # Frontend UI
├── static/
│   └── style.css        # Custom styling
├── app.py               # Main Flask Application
├── store_index.py       # Script to ingest data into Pinecone
├── Dockerfile           # Docker configuration
├── requirements.txt     # Python dependencies
└── .env                 # API Keys (Not uploaded to GitHub)

💻 Local Installation & Setup
1. Clone the Repository
Bash

git clone [https://github.com/your-username/Medical-Chatbot-RAG.git](https://github.com/your-username/Medical-Chatbot-RAG.git)
cd Medical-Chatbot-RAG
2. Create a Virtual Environment
Bash

python -m venv medienv
Activate the environment:

Windows: medienv\Scripts\activate

Mac/Linux: source medienv/bin/activate

3. Install Dependencies
Bash

pip install -r requirements.txt
4. Setup Environment Variables
Create a .env file in the root directory and add your keys:

Ini, TOML

PINECONE_API_KEY=your_pinecone_api_key
OPENAI_API_KEY=your_openai_api_key
5. Ingest Data (Run Once)
This script loads the PDF, chunks it, creates embeddings, and uploads them to Pinecone.

Bash

python store_index.py
6. Run the Application
Bash

python app.py
Open your browser and go to: http://localhost:8080