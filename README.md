# Simple RAG System Tutorial & WE Telecom Customer Agent
This Repo is for educational purposes of how to implement a RAG System.
This project provides a step-by-step introduction to Vector Databases and how to build a Retrieval-Augmented Generation (RAG) pipeline from scratch. We demonstrate the practical application of RAG by building a **Customer Agent for WE Telecom** that can answer queries based on Scraped Data from their website.

## 📂 Project Structure

- `Intro_to_VectorDB.ipynb`
  A beginner-friendly notebook explaining the fundamentals of RAG, text embeddings, and vector databases. It uses a local, in-memory instance of the Qdrant vector database.
- `RAG_Simple.ipynb`
  An end-to-end implementation of a simple RAG system. It connects to **Qdrant Cloud** to index documents and uses Hugging Face models (`sentence-transformers/all-MiniLM-L6-v2` as the encoder and `vblagoje/bart_lfqa` as the generator) to answer WE Telecom customer queries.
- `WE_Telecom_en/`
  A directory containing markdown documents about WE Telecom (e.g., prepaid/postpaid plans, internet packages, board of directors). This serves as our knowledge base.

## 🛠️ Prerequisites

To run these notebooks, you need a Python environment with the following dependencies:

```bash
pip install numpy sentence-transformers qdrant-client transformers
```
*(Note: If you run these notebooks in Google Colab, the installation commands are already included in the first cells.)*

For the `RAG_Simple.ipynb` notebook, you will also need a **free Qdrant Cloud account**:
1. Go to [Qdrant Cloud](https://cloud.qdrant.io/) and create an account.
2. Create a free-tier cluster.
3. Retrieve your **Cluster URL** and **API Key** from the cluster details panel.

## 🚀 How to Use

1. **Clone or Download** this repository to your local machine (or upload it to Google Colab).
2. **Install the required packages** as shown above.
3. **Start with `Intro_to_VectorDB.ipynb`** to understand the foundational concepts of embedding text and storing vectors locally.
4. **Proceed to `RAG_Simple.ipynb`**, where you will input your Qdrant Cloud credentials, embed the markdown files inside `WE_Telecom_en/`, and interact with the generative AI model to answer questions based on the documentation.

## 🧠 What You Will Learn

- How **Text Embeddings** convert human-readable text into mathematical representations (vectors).
- How **Vector Databases** (Qdrant) store and rapidly search through embeddings using Cosine Similarity.
- The two phases of RAG: **Data Ingestion** and **Query Generation**.
- How to connect a **Retriever** (vector search) with a **Generator** (LLM like BART) to produce accurate, context-aware answers without fine-tuning.
