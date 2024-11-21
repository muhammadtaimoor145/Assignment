# Assignment
Crime and Punishment Book Summarizer with FAISS and OpenAI
Overview
This project is a summarization tool designed to process the book Crime and Punishment by Fyodor Dostoevsky. The tool uses the Sentence-Transformers/all-mpnet-base-v2 model for sentence embeddings and FAISS for storing and searching the embeddings. Each page of the book is indexed with its metadata (page number), and OpenAI's API is used to generate summaries based on the retrieved content from specific pages.

Key Features:
Embeddings: Utilizes Sentence-Transformers/all-mpnet-base-v2 to generate high-quality sentence embeddings.
FAISS Indexing: FAISS is used to index the book's content based on sentence embeddings for efficient retrieval.
Page Number as Metadata: Each page's content is indexed along with its page number for precise retrieval and context.
OpenAI Summaries: OpenAI's API is used to generate high-level summaries based on the content retrieved from the FAISS index.
Components
1. Sentence-Transformers
This model, all-mpnet-base-v2, is used to generate sentence embeddings, which are vector representations of the text. This is a pre-trained model from sentence-transformers that works well for semantic text similarity tasks.

2. FAISS
FAISS is used to index and search large-scale embeddings efficiently. The embeddings of each page are indexed in FAISS, which allows for rapid similarity search when querying based on page numbers or summary requests.

3. OpenAI GPT
OpenAI's language models are used to generate high-level summaries based on the retrieved page content. This tool takes the page embeddings, extracts relevant content, and generates a concise summary.

4. Page Numbers as Metadata
Each page of the book is indexed with its corresponding page number, enabling precise queries for content from a specific page range or section of the book.

Requirements
Python 3.x
Libraries:
sentence-transformers (for generating sentence embeddings)
faiss-cpu or faiss-gpu (for efficient similarity search)
openai (for querying the OpenAI API)
FPDF (for creating PDF summaries)
You can install the required libraries using pip:

bash
Copy code
pip install sentence-transformers faiss-cpu openai fpdf
Setup Instructions
Step 1: Install Dependencies
Ensure all necessary dependencies are installed. Use the command below to install the required libraries.

bash
Copy code
pip install sentence-transformers faiss-cpu openai fpdf
Step 2: Download or Load the Book
You will need the text content of Crime and Punishment. You can either provide the text manually or extract it from a public domain source.

Step 3: Embedding the Book
The first step is to generate sentence embeddings for each page of the book. These embeddings are stored in FAISS, where each sentence is associated with its page number.

Step 4: Store and Index the Embeddings
The sentence embeddings are stored in a FAISS index, allowing fast retrieval of similar content based on a query. Each page's text is indexed along with the page number for reference.

Step 5: Querying OpenAI for Summaries
When you make a query, the system will retrieve relevant pages using FAISS, pass the content to OpenAI's API, and generate summaries. The query can be based on specific page ranges or questions about the book's content.
