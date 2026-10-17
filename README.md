# PDF Intelligence: Semantic Retrieval System

## Overview

This project implements a PDF-based semantic retrieval pipeline that extracts text from PDF documents, converts the text into overlapping chunks, generates sentence embeddings, and retrieves relevant content based on a user's query.

## Key Features

* **PDF Text Extraction:** Extracts text from PDF documents using PyMuPDF.
* **Text Chunking:** Splits extracted text into overlapping chunks for better retrieval.
* **Semantic Embeddings:** Uses the Sentence Transformers `all-MiniLM-L6-v2` model to generate text embeddings.
* **Vector Similarity Search:** Uses FAISS to efficiently retrieve relevant chunks.
* **Source Tracking:** Displays source document names, chunk indices, and similarity distances.
* **Batch Queries:** Supports testing multiple questions against the document collection.

## Tech Stack

* Python
* PyMuPDF
* Sentence Transformers
* FAISS
* NumPy
* JSON
* Kaggle Notebooks

## How It Works

1. Load PDF documents from the dataset.
2. Extract text from each PDF.
3. Split the text into chunks with overlapping content.
4. Generate vector embeddings for the chunks.
5. Build a FAISS index for similarity search.
6. Encode a user query and retrieve the most relevant text chunks.
7. Display the retrieved content and its source information.

## Configuration

* **Embedding Model:** `all-MiniLM-L6-v2`
* **Chunk Size:** 150 words
* **Chunk Overlap:** 30 words
* **Top-K Retrieval:** 3 chunks

## Project Status

The current implementation focuses on document retrieval and semantic search. It does not yet include a generative language model for composing answers from retrieved passages.

## Future Improvements

* Integrate an LLM to generate answers grounded in retrieved documents.
* Add a user-friendly web interface.
* Improve retrieval evaluation and document handling.

## Author

**Abhinav Pal**
MTech Research Student, Delhi Technological University (DTU)
