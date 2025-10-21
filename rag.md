🔷 PHASE 1: Fundamentals
1. Understand the Motivation Behind RAG

Why do we need retrieval?

Limitations of closed-book LLMs.

Open-domain question answering (ODQA) vs. closed-book QA.

📚 Resources:

Lewis et al. (2020) RAG Paper

“Attention is All You Need” for Transformer fundamentals.

🔷 PHASE 2: Core Components of RAG
2. RAG Architecture Overview

Dual system: Retriever + Generator

Pipeline vs. End-to-End (e.g., Fusion-in-Decoder)

Chunking + Embedding + Retrieval + Reranking + Prompt Construction + Generation

🔶 PHASE 3: The Retriever
3. Data Chunking

Fixed-size vs. semantic chunking

Window size, overlap

Recursive chunking with tools like LangChain, LlamaIndex

4. Embedding Techniques

Sentence-transformers (all-MiniLM, multi-qa-mpnet)

OpenAI Embeddings (text-embedding-ada-002)

Cohere, Hugging Face Transformers

5. Vector Stores

FAISS, Pinecone, Weaviate, Qdrant, Milvus, Chroma

Flat vs. HNSW indexing

6. Indexing

Dense Indexing (embedding-based)

Sparse Indexing (BM25, TF-IDF)

Hybrid Indexing (Dense + Sparse fusion)

7. Retrieval Techniques

k-NN search

ANN (Approximate Nearest Neighbor) retrieval

Reranking:

Cross-encoders (ColBERT, monoBERT)

DPR (Dense Passage Retrieval)

Splade (sparse retriever)

📚 Tools:

faiss, haystack, gpt-index, langchain, transformers

🔶 PHASE 4: The Generator
8. Prompt Construction

Use of context windows

Condensing retrieved results

Prompt injection (metadata, source links)

Prompt compression (Map-Reduce, Refinement)

9. Language Models

OpenAI (GPT-4, GPT-3.5)

Anthropic (Claude)

Mistral, LLama, Falcon (open-source)

Instruction-tuned vs. base models

📚 Skill:

Prompt Engineering

Managing context length

Few-shot, Chain-of-Thought prompting

🔷 PHASE 5: Types of RAG Architectures
10. Types of RAG
Type	Description
Basic RAG	Fixed retriever + generator
RAG-Sequence	Retrieve for each generation step
RAG-Token	Retrieve per token
Fusion-in-Decoder (FiD)	Fuses multiple contexts before generation
REALM / DPR	Pretrained retriever integration
HyDE	Hypothetical Document Embeddings
🔶 PHASE 6: Advanced Topics
11. Fine-Tuning Retrievers

DPR fine-tuning using contrastive loss

In-domain adaptation

Negative sampling strategies

12. Evaluating RAG Systems

Precision/Recall for retriever

BLEU, ROUGE, METEOR for generator

Human evaluation

Hallucination analysis

13. Caching Strategies

Embedding caching

Context caching

Retrieval result caching for performance

14. Multi-modal RAG

Use images/audio/video + text (CLIP, Flamingo, LLaVA)

15. Multi-hop Retrieval

Retrieval chains

Document traversal strategies (QA chains)

🔷 PHASE 7: Tools & Frameworks
16. Key Libraries

LangChain

LlamaIndex

Haystack

Hugging Face Transformers

Unstructured.io (for document preprocessing)

Chroma, Qdrant, Pinecone (vector dbs)

17. Deployment

API Design (FastAPI, Flask)

Streaming generation

Cost optimization (e.g., rerank only top-k, reduce model calls)

🔶 PHASE 8: Projects to Build
18. Mini Projects (Hands-on)

PDF Q&A bot: Upload a PDF and ask questions

Slack RAG assistant: Connect RAG bot to a team’s Slack

Code search engine: Query across large codebase

Academic paper assistant: Semantic search + summarization

Legal assistant: Query over contracts

🔶 PHASE 9: Stay Updated
19. Follow the Latest Developments

Papers with Code: RAG

ArXiv weekly (subscribe to NLP section)

GitHub repos: facebookresearch/DPR, huggingface/transformers, LangChainAI/langchain
