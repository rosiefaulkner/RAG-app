# 📄 RAG App with DeepSeek R1 & Ollama

This project is a lightweight **Retrieval-Augmented Generation (RAG)** application built with [Streamlit](https://streamlit.io/) and powered by **DeepSeek R1** via [Ollama](https://ollama.com/). Upload a PDF, ask questions, and get context-aware answers using semantic search and local LLM inference.

---

## 🔧 Features

* 📥 Upload any PDF file.
* 🧠 Semantic chunking of document content using HuggingFace embeddings.
* 🔍 Efficient document retrieval using FAISS vector store.
* 🤖 Natural language answers generated with the DeepSeek R1 LLM.
* 💬 Real-time Q\&A interface via Streamlit.

---

## 🧱 Tech Stack

* **Streamlit** – UI for file upload and interaction
* **PDFPlumberLoader** – PDF text extraction
* **SemanticChunker** – Document chunking using semantic embeddings
* **HuggingFaceEmbeddings** – Embedding model for document vectors
* **FAISS** – Vector similarity search
* **Ollama** – Local LLM runner using `deepseek-r1:1.5b`
* **LangChain** – Modular chains and prompt management

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone [https://github.com/rosiefaulkner/RAG-app.git](https://github.com/rosiefaulkner/RAG-app.git)
cd RAG-app
```

### 2. Install dependencies

Ensure you have Python 3.10+ and create a virtual environment.

```bash
pip install -r requirements.txt
```

### 3. Start Ollama and Pull the Model

Make sure [Ollama](https://ollama.com/download) is installed and the DeepSeek model is pulled:

```bash
ollama run deepseek-r1:1.5b
```

> Leave Ollama running in the background for the LLM to function properly.

### 4. Run the Streamlit app

```bash
streamlit run app.py
```

---

## 📂 How It Works

1. Upload a `.pdf` file.
2. The PDF is processed and semantically chunked into smaller segments.
3. Each chunk is embedded and stored in a FAISS vector database.
4. A question is input by the user.
5. The top 3 most relevant chunks are retrieved via vector similarity search.
6. These chunks are passed to a DeepSeek R1 model via Ollama to generate a response.

---

## ✍️ Example Usage

1. Upload `example_invoice.pdf`
2. Ask: *"What is the total balance due?"*
3. Get an instant, contextual answer like:
   **Response:** *The total balance due is \$4,500.*

---

## 📌 Notes

* This app is for local use; no data is sent to the cloud.
* Ensure that your machine has sufficient RAM and CPU to run local LLMs efficiently.

---

## 🧠 Future Enhancements

* ✅ Multi-document support
* ✅ LLM model switcher (e.g., Mixtral, LLaMA3, etc.)
* ✅ Export Q\&A logs
* ✅ Summarization mode

---

## 🛡️ License

MIT License

---

## 🙌 Resources

* [LangChain](https://www.langchain.com/)
* [Ollama](https://ollama.com/)
* [HuggingFace](https://huggingface.co/)
* [Streamlit](https://streamlit.io/)

---

Let me know if you'd like the `requirements.txt` generated too or if this README should include example screenshots.
