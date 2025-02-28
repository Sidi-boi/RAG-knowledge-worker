# Expert Knowledge Worker using RAG

## Overview
This project implements a **Retrieval-Augmented Generation (RAG)** system that allows users to interact with a chatbot powered by OpenAI's language model and enhanced with a vector database for knowledge retrieval. The chatbot retrieves relevant information from a knowledge base and provides accurate responses based on stored documents.

## Features
- **Document Ingestion**: Loads text-based documents from a knowledge base.
- **Text Chunking**: Splits documents into smaller chunks for efficient vector storage.
- **Vectorization**: Uses OpenAI embeddings to create a searchable vector database with **ChromaDB**.
- **Interactive Chatbot**: Implements a conversational AI with memory and knowledge retrieval.
- **Data Visualization**: Provides 2D and 3D visualizations of document embeddings using **t-SNE** and **Plotly**.
- **Gradio Interface**: Offers a web-based chat interface for user interaction.

## Installation
### Prerequisites
Ensure you have Python 3.10+ installed. Install the required dependencies using:
```bash
pip install -r requirements.txt
```
### Required Environment Variables
Create a `.env` file and add your OpenAI API key:
```ini
OPENAI_API_KEY=your-api-key-here
```

## Usage
### 1. Load and Process Documents
The system loads text documents from the `knowledge-base/` directory and assigns metadata to them.

### 2. Vectorize Documents
The documents are embedded using OpenAI embeddings and stored in a **ChromaDB** vector database.

### 3. Data Visualization
The stored embeddings are visualized using **t-SNE** in **2D** and **3D** for better interpretability.

### 4. Chatbot Interaction
Run the chatbot using Gradio:
```bash
python main.py
```
The chatbot interface will launch in the browser.

## Project Structure
```
├── knowledge-base/        # Directory containing text documents
├── main.py                # Main execution script
├── requirements.txt       # Required dependencies
├── .env                   # Environment variables
└── README.md              # Project documentation
```

## Technologies Used
- **Python** (3.10)
- **LangChain** for document processing & RAG
- **OpenAI GPT-4o-mini** for LLM
- **ChromaDB** for vector storage
- **Gradio** for chat interface
- **t-SNE** & **Plotly** for visualization

## Future Enhancements
- Support for additional document formats (PDF, CSV, etc.)
- Integration with external APIs for real-time knowledge updates
- Enhanced conversation memory management

