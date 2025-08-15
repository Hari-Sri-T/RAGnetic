# RAGnetic – Retrieval-Augmented Generation Pipeline

RAGnetic is a **document question-answering system** powered by a **Retrieval-Augmented Generation (RAG)** architecture.  
It ingests your documents, indexes them with vector embeddings, and answers natural language queries with accurate, context-aware responses using Microsofts phi3 model.

---

## Prerequisites:

- Need Ollama locally installed with phi3 model downloaded in it.
- Need atleast 16gb ram to be working without crashes

##  Features

- Multi-format document ingestion – PDF, DOCX, and text files supported.  
- Chunking – Splits documents into manageable sections for better retrieval.  
- Vector storage with FAISS – Fast and scalable similarity search.  
- Context-aware answers – Combines retrieved chunks with LLM generation.  
- Local or API-based LLM support – Works with models like LLaMA, Nous Hermes, GPT, etc.  
- Customizable – Swap out embedding models, chunk sizes, and retrieval parameters.  

---

##  Tech Stack

- Python – Core implementation  
- FAISS – Vector similarity search  
- Ollama / Hugging Face models – Local LLM inference  
- Transformers – Embedding & generation  
- FastAPI – API interface for integration  

---

##  Project Structure

RAG_pipeline/  
├── data/                # Your documents  
├── embeddings/          # Vector database storage  
├── RAG_pipeline.ipynb   # Main pipeline notebook  
├── requirements.txt     # Python dependencies  
└── README.md            # Documentation  

---

##  Installation

1. **Clone this repository**  
   git clone https://github.com/Hari-Sri-T/RAGnetic
   cd RAGnetic

2. **Install dependencies**  
   pip install -r requirements.txt  

3. **(Optional) Install FAISS with GPU support**  
   pip install faiss-gpu  

---

##  Usage

1. Add your documents to the same folder and modify the file path in the jupyter notebook. 
2. Get Ollama model phi3 running in the back.
3. Run the pipeline in the Jupyter notebook:  
   jupyter notebook RAG_pipeline.ipynb  
4. Ask questions in natural language — get context-aware answers from your docs.  

---

##  How It Works

1. **Document Ingestion** – Reads & preprocesses PDFs/DOCX/text.  
2. **Chunking** – Splits into overlapping chunks.  
3. **Embedding** – Converts text to dense vectors.  
4. **Storage** – Saves vectors in FAISS index.  
5. **Retrieval** – Finds the most relevant chunks for a query.  
6. **Generation** – Passes chunks + query to an LLM for final answer.  

---

## License

This project is licensed under the MIT License.

