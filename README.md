
This Streamlit application leverages Langchain, Groq, and FAISS to create an interactive Q&A system based on document embeddings. Users can input questions and receive accurate responses extracted from a set of documents. The application includes the following key features:

Environment Setup: Load API keys from environment variables using dotenv.

Streamlit Interface: Set up the Streamlit user interface with a title and input fields for user interaction.
LLM Initialization: Use Groq's ChatGroq model for generating responses based on context.

Prompt Template: Define a prompt template to format the context and questions for the LLM.

Vector Embedding Function:
Load and preprocess documents from a specified directory using PyPDFDirectoryLoader.
Split documents into chunks with RecursiveCharacterTextSplitter.
Generate embeddings using Google's Generative AI Embeddings.
Store embeddings in a FAISS vector store.

User Interaction:
A text input field allows users to enter questions.
A button triggers the embedding process and prepares the vector store.

📘 README.md
# Document Q&A with Groq, LangChain & Streamlit 📄🤖

This project is a **Document Question Answering (Q&A) system** that enables users to ask questions from PDF documents using **LangChain**, **Groq LLM (Llama 3)**, and **Google Generative AI embeddings**.

The application processes PDFs, creates vector embeddings, stores them using **FAISS**, and retrieves relevant context to generate accurate answers via a Streamlit interface.

---

## 🚀 Features

- PDF document ingestion
- Text chunking for efficient retrieval
- Vector embeddings using Google Generative AI
- FAISS-based vector search
- Context-aware answers using Groq LLM (Llama 3)
- Interactive Streamlit UI
- Document similarity inspection

---

## 🧠 How It Works

1. **Document Loading**
   - PDFs are loaded from a local directory

2. **Text Splitting**
   - Documents are split into overlapping chunks

3. **Embedding Creation**
   - Chunks are converted into embeddings

4. **Vector Storage**
   - Embeddings are stored in FAISS

5. **Retrieval & Answering**
   - Relevant chunks are retrieved
   - LLM answers based only on retrieved context

---

## 📂 Project Structure

```text
.
├── us_census/              # PDF documents directory
├── app.py                  # Streamlit application
├── requirements.txt
└── README.md

▶️ Setup Instructions
1️⃣ Clone the Repository
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

2️⃣ Create Virtual Environment
python -m venv venv
source venv/bin/activate     # Windows: venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

🔐 Environment Variables
Create a .env file in the project root:
GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
Do not push this file to GitHub unless you enjoy key rotation.

▶️ Run the Application
streamlit run app.py

Usage Flow:
Click Documents Embedding to initialize vector store
Enter your question
View the answer and related document chunks

🛠️ Tech Stack
Python
Streamlit
LangChain
Groq (Llama 3)
Google Generative AI Embeddings
FAISS
dotenv

⚠️ Notes
Designed for learning and demos
Works best with clean, text-heavy PDFs
Not optimized for large-scale document collections

Query Processing:
Retrieve and process user questions.
Use a retrieval chain to find relevant document chunks and generate answers.
Show the response and the relevant document chunks in a Streamlit expander for context.
This application provides a user-friendly interface for querying document-based information, making it a powerful tool for extracting insights from large sets of documents.
