# agentic-rag

Agentic RAG Pipeline for WebMD Health Information Retrieval
This project demonstrates an Agentic Retrieval-Augmented Generation (RAG) workflow using LangChain, designed to answer medical and health-related questions by retrieving and reasoning over authoritative content from WebMD articles.

Pipeline Steps:

- Data Source Collection – Fetched medical articles from WebMD covering topics like allergies, arthritis, cancer, depression, and flu.

- Text Extraction & Preprocessing – Parsed HTML pages using BeautifulSoup to extract clean text content.

- Text Chunking – Split extracted text into overlapping segments using LangChain’s RecursiveCharacterTextSplitter for better retrieval granularity.

- Embedding Generation – Generated semantic embeddings for each chunk using HuggingFaceHubEmbeddings (sentence-transformers family).

- Vector Store Creation – Stored embeddings in ChromaDB for fast and relevant document retrieval.

- Agentic RAG Construction – Integrated a retriever tool into an agent powered by Groq-hosted LLMs to enable multi-step reasoning and selective retrieval.

- Query Processing – The agent interprets user health queries, retrieves relevant medical context, and generates concise, medically relevant responses.