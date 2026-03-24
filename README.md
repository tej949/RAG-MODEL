# RAG Model - Retrieval-Augmented Generation with Krypt Documentation

A Retrieval-Augmented Generation (RAG) system that processes and indexes documentation from the Krypt blockchain project, enabling intelligent document retrieval and question-answering capabilities.

## Project Overview

This project implements a RAG pipeline that:
- Ingests multiple document formats (PDF, Markdown, CSV)
- Processes documents using LangChain and sentence transformers
- Stores embeddings in ChromaDB vector store
- Enables semantic search and retrieval-augmented generation

## Features

- **Multi-format Document Support**: Process PDFs, Markdown, and text files
- **Vector Embeddings**: Uses sentence-transformers for semantic understanding
- **Persistent Vector Store**: ChromaDB for efficient similarity searches
- **LLM Integration**: Groq API integration for generative tasks
- **Modular Architecture**: Clean separation of concerns for extensibility

## Tech Stack

- **LangChain**: Document processing and RAG orchestration
- **ChromaDB**: Vector database for embeddings storage
- **Sentence Transformers**: Semantic embedding generation
- **Groq**: LLM API for generative responses
- **PyMuPDF & PyPDF**: PDF document parsing
- **FAISS**: CPU-based similarity search

## Project Structure

```
RAG_model/
├── data/
│   ├── notion/          # Notion exports (.md, .csv)
│   ├── pdf/             # PDF documents
│   ├── text_files/      # Text files
│   └── vector_store/    # ChromaDB persisted data
├── notebook/
│   ├── document.ipynb   # Main processing notebook
│   └── pdf_loader.ipynb # PDF loading utilities
├── src/                 # Source code modules
├── main.py              # Entry point
├── requirements.txt     # Project dependencies
└── README.md
```

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd RAG_model
   ```

2. **Create virtual environment** (Python 3.13+)
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Add your Groq API key and other configuration
   ```

## Usage

### Running the RAG Pipeline

```bash
python main.py
```

### Jupyter Notebooks

- **[document.ipynb](notebook/document.ipynb)**: Main data processing pipeline
- **[pdf_loader.ipynb](notebook/pdf_loader.ipynb)**: PDF extraction and loading utilities

### Document Processing

The system processes documents from `data/` directories:
- PDFs from `data/pdf/`
- Notion exports from `data/notion/`
- Text files from `data/text_files/`

Vector embeddings are stored in `data/vector_store/` using ChromaDB.

## Configuration

Update `.env` file with:
```
GROQ_API_KEY=your_api_key_here
```

## Dependencies

See [requirements.txt](requirements.txt):
- langchain & langchain ecosystem
- chromadb (vector database)
- sentence-transformers (embeddings)
- pymupdf & pypdf (PDF processing)
- faiss-cpu (similarity search)

## Document Set

This project indexes the **Krypt** blockchain project documentation:
- React + Solidity decentralized application for Ethereum transactions
- Smart contract code and frontend implementation details
- Project report and technical specifications

## Future Enhancements

- [ ] Support for additional document formats (DOCX, HTML)
- [ ] Real-time document updates
- [ ] Multi-language support
- [ ] Advanced query expansion techniques
- [ ] Hybrid search (semantic + keyword)
- [ ] Web UI for document exploration

## License

MIT License 

## Author

Tejomai V 
