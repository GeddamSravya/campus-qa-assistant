\# Campus Q\&A Assistant



A Retrieval-Augmented Generation (RAG) based university question-answering assistant that retrieves information from the official GNITS website and generates answers using Google Gemini.



\## Project Overview



The Campus Q\&A Assistant allows users to ask questions about university information.



The system retrieves relevant information from the GNITS website using both semantic vector similarity and keyword-based retrieval, combines the results using hybrid score fusion, reranks the retrieved content, and uses Gemini to generate the final answer.



\## Architecture



GNITS Official Website

&#x20;       ↓

Document Loading

&#x20;       ↓

Document Chunking

&#x20;       ↓

Gemini Embeddings

&#x20;       ↓

Vector Similarity Search

&#x20;       +

BM25 Keyword Search

&#x20;       ↓

Hybrid Score Fusion

&#x20;       ↓

Top-K Retrieval

&#x20;       ↓

Reranking

&#x20;       ↓

Top-N Context

&#x20;       ↓

Query Rewriting

&#x20;       ↓

Conversation Memory

&#x20;       ↓

Google Gemini LLM

&#x20;       ↓

Final Answer + Source



\## Features



\- Web document loading

\- Document chunking with overlap

\- Gemini text embeddings

\- Vector similarity search

\- BM25 keyword retrieval

\- Hybrid retrieval using score fusion

\- Top-K retrieval and reranking

\- Query rewriting for follow-up questions

\- Conversation memory

\- Gemini LLM-based answer generation

\- Source information in responses

\- Context-grounded answers to reduce unsupported responses



\## Technologies Used



\- Python

\- LangChain

\- Google Gemini

\- Gemini Embeddings

\- BM25

\- Chroma

\- NumPy

\- BeautifulSoup

\- Jupyter Notebook



\## Project Files



\- `campus\_qa.ipynb` - Main project notebook

\- `requirements\_current.txt` - Python dependencies

\- `.gitignore` - Prevents sensitive and environment files from being uploaded



\## How It Works



1\. The GNITS official website is loaded as the source document.

2\. The document is divided into smaller chunks.

3\. Gemini embeddings are generated for the chunks.

4\. BM25 creates a keyword-based retrieval index.

5\. A user question is converted into an embedding.

6\. Vector similarity and BM25 scores are calculated.

7\. Both scores are combined using hybrid score fusion.

8\. The top relevant chunks are selected and reranked.

9\. Conversation history is used for follow-up questions.

10\. The retrieved context is provided to Gemini.

11\. Gemini generates the final answer using the retrieved context.

12\. Source information is returned with the answer.



\## Example Questions



```text

What courses are offered by GNITS?



What about the engineering courses?



Which of them are related to computer science?

