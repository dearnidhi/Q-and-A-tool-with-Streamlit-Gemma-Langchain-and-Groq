Description:
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

Query Processing:
Retrieve and process user questions.
Use a retrieval chain to find relevant document chunks and generate answers.

Display Results:
Show the response and the relevant document chunks in a Streamlit expander for context.
This application provides a user-friendly interface for querying document-based information, making it a powerful tool for extracting insights from large sets of documents.
