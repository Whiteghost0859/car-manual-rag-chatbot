# car-manual-rag-chatbot
A context-aware RAG chatbot using LangChain and OpenAI to navigate technical car manual documentation.

# Technical Documentation RAG Chatbot

An implementation of a Retrieval-Augmented Generation (RAG) pipeline built using LangChain, OpenAI's `gpt-4o-mini`, and Chroma DB to build a context-aware chatbot capable of answering complex user troubleshooting queries from a vehicle service manual.

## 🛠️ Tech Stack & Tools
- **Framework:** LangChain (LCEL)
- **LLM:** OpenAI `gpt-4o-mini`
- **Vector Database:** Chroma DB
- **Data Splitting:** Recursive Character Text Splitter

## 🚀 Key Pipeline Steps Implemented
1. **Document Processing:** Loaded and parsed raw HTML warning logs from an SUV user manual.
2. **Chunking & Semantic Bridging:** Chunked texts using a balanced size of 500 characters with a 50-character overlap to preserve critical warning syntax.
3. **Vector Embeddings:** Embedded text chunks and indexed them inside a high-performance vector store (Chroma).
4. **Targeted Retrieval:** Configured a similarity retriever optimized at $k=1$ to pull hyper-specific dashboard alerts without introducing hallucinated noise.
5. **LCEL Chain Composition:** Bound components together using LangChain Expression Language for instant query execution.
