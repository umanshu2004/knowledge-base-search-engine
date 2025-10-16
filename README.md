# knowledge-base-search-engine
This project is a powerful search engine that uses a Large Language Model (LLM) to answer questions based on a collection of documents you provide. It leverages Retrieval-Augmented Generation (RAG) to find the most relevant information in your documents and then uses that information to generate a concise, synthesized answer to your query.

**Objective**

The main goal of this project is to provide a way to search across multiple text and PDF documents and receive synthesized, context-aware answers. Instead of just pointing to relevant documents, the system directly answers the user's questions based on the content of those documents.

**How It Works**

Document Ingestion: You can upload your text or PDF documents through the web interface.

Processing & Embedding: The backend processes these documents, breaks them down into smaller chunks, and creates numerical representations (embeddings) of each chunk using a sophisticated AI model. These embeddings are stored for later retrieval.

User Query: You ask a question through the search interface.

Retrieval: The system converts your question into an embedding and compares it to the stored document embeddings to find the most relevant chunks of text.

Answer Synthesis: The relevant text chunks are passed to an LLM along with your original question. The LLM then generates a human-like, synthesized answer based on the provided context.

**Technical Stack
**
Backend: Python with Flask (a lightweight web framework)

**Core Logic:**

langchain: A framework for developing applications powered by language models.

faiss-cpu: A library for efficient similarity search, used here to find relevant document chunks.

sentence-transformers: A library for creating high-quality embeddings.

PyMuPDF: For extracting text from PDF documents.

Frontend: A simple, clean interface built with HTML, styled with Tailwind CSS, and powered by vanilla JavaScript for interactivity.

**Getting Started**

Prerequisites

Python 3.8 or higher

pip (Python package installer)

**Installation**

Clone the repository:

git clone <your-repo-url>
cd <your-repo-name>


Install the required Python packages:

pip install Flask langchain faiss-cpu sentence-transformers PyMuPDF


(Note: Depending on your system, you might need to install other dependencies like build tools for faiss-cpu.)

Run the Flask application:

python app.py


Open your web browser and navigate to http://127.0.0.1:5000. You should see the search engine's interface.

How to Use the Application

Upload Documents: Click the "Choose Files" button to select one or more .txt or .pdf files from your computer.

Ask a Question: Once the files are uploaded and processed (you'll see a confirmation message), type your question into the search box.

Get an Answer: Press Enter or click the "Ask" button. The synthesized answer will appear below the search box.

Project Structure

.
├── app.py              # The main Flask application with all backend logic.
├── templates/
│   └── index.html      # The HTML file for the frontend user interface.
└── README.md           # This file.


This project provides a solid foundation for a sophisticated, LLM-powered search engine. It's designed to be clear, and easy to understand, making it a great starting point for further enhancements and customizations.
