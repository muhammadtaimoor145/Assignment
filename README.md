# Assignment
Crime and Punishment Book Summarizer with FAISS and OpenAI
Overview
This project is a summarization tool designed to process the book Crime and Punishment by Fyodor Dostoevsky. The tool uses the **Sentence-Transformers/all-mpnet-base-v2** model for sentence embeddings and **FAISS** for storing and searching the embeddings. Each page of the book is indexed with its metadata (page number), and OpenAI's API is used to generate summaries based on the retrieved content from specific pages.

Key Features:
Embeddings: Utilizes Sentence-Transformers/all-mpnet-base-v2 to generate high-quality sentence embeddings.
FAISS Indexing: FAISS is used to index the book's content based on sentence embeddings for efficient retrieval.
Page Number as Metadata: Each page's content is indexed along with its page number for precise retrieval and context.
OpenAI Summaries: OpenAI's API is used to generate high-level summaries based on the content retrieved from the FAISS index.
Components
**Page Numbers as Metadata
**  : Each page of the book is indexed with its corresponding page number, enabling precise queries for content from a specific page range or section of the book.

For Dependency Installation, Plz run following requirements.txt
```bash
pip install -r requirements.txt
