
# 📄 RAG Q\&A System

## Overview

The **RAG (Retrieval-Augmented Generation) Q\&A System** combines retrieval-based search with generative models to answer questions using content extracted from websites or PDFs. This hybrid approach ensures more accurate and contextually relevant answers.

---

## 🔧 Setup Instructions

Install the required dependencies:

```bash
pip install langchain langchain-community transformers gradio requests beautifulsoup4 faiss-cpu
```

* **langchain** and **langchain-community**: For building chains and retrieval pipelines.
* **transformers**: For pre-trained generative models like BART.
* **gradio**: For creating the web interface.
* **requests & beautifulsoup4**: For web scraping.
* **faiss-cpu**: For vector similarity search.

---

## 🧠 How It Works

1. **Scraping / Loading Documents**: Extracts content from specified websites or PDFs.
2. **Text Splitting**: Divides large texts into smaller chunks using `RecursiveCharacterTextSplitter`.
3. **Embeddings**: Converts text chunks into vector embeddings with `HuggingFaceEmbeddings`.
4. **Vector Store**: Stores embeddings in FAISS for efficient retrieval.
5. **Retrieval + Generation**: Answers questions by retrieving relevant chunks and generating answers using a HuggingFace pipeline (e.g., `facebook/bart-large-cnn`).

---

## 🚀 Usage

1. **Run the Notebook**: Execute all cells to prepare the retrieval and generation pipeline.
2. **Gradio Interface**: A web interface will launch, allowing you to input questions.
3. **Ask Questions**: Type any query related to the loaded websites/PDFs.
4. **Receive Answers**: The system retrieves relevant context and generates an answer.

---

## 🔄 Example

**Question**:
*"What information is available from these websites?"*

**Answer**:
*The system searches through the scraped content and provides a concise, context-aware response.*

---

## 📝 Notes

* The notebook currently scrapes these websites:

  * [DOAJ](https://doaj.org)
  * [OpenStax](https://openstax.org)
  * [Wikibooks](https://en.wikibooks.org)

* If running on a CPU, responses may take longer compared to using a GPU.

* Make sure your environment has compatible versions of PyTorch, Transformers, and Protobuf to avoid errors.

---

## 📄 License

This project is licensed under the MIT License.

---


