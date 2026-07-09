# RAG-Document-QA

A simple Retrieval-Augmented Generation (RAG) application that allows users to upload a PDF document and ask questions about its contents. The project uses a local language model along with vector embeddings to retrieve relevant information from the uploaded document before generating responses.

## Features

- Upload PDF documents
- Extract and process text from PDFs
- Automatic text chunking
- Generate embeddings using Sentence Transformers
- Store embeddings in ChromaDB
- Ask natural language questions about the document
- Local LLM inference (No OpenAI API required)
- Simple Streamlit-based user interface

## Tech Stack

- Python
- Streamlit
- LangChain
- ChromaDB
- Sentence Transformers
- Hugging Face Transformers
- LaMini-T5-738M
- PDFMiner

## Project Structure

```
.
├── chatbot_app.py      # Main Streamlit application
├── ingest.py           # PDF ingestion and vector database creation
├── constants.py        # ChromaDB configuration
├── docs/               # Uploaded PDF documents
├── db/                 # Persisted vector database
├── requirements.txt
└── README.md
```

## How it Works

1. Upload a PDF document.
2. Extract text from the PDF.
3. Split the text into smaller chunks.
4. Generate embeddings for each chunk.
5. Store embeddings in ChromaDB.
6. Convert user queries into embeddings.
7. Retrieve the most relevant chunks.
8. Generate an answer using a local language model.

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/chat-with-pdf.git
cd chat-with-pdf
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create the required directories:

```bash
mkdir docs
mkdir db
```

## Run the Application

Start the Streamlit app:

```bash
streamlit run chatbot_app.py
```

Open your browser and upload a PDF to begin chatting with your document.

## Future Improvements

- Support multiple PDF documents
- Display source citations
- Improve retrieval quality with reranking
- Conversation memory
- Support larger language models
- Docker Compose deployment

## License

This project is licensed under the MIT License.
