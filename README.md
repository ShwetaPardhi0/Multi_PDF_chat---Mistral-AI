# 📚 Multi-PDF Chatbot with Mistral-7B + LangChain

This project allows you to **chat with multiple PDF documents** using a **local Mistral-7B model** with `llama-cpp-python`, LangChain, FAISS, and Streamlit.  
It supports both **command-line interaction** and a **Streamlit web app** interface.  

---

## 🚀 Features
- Load multiple PDFs and extract text with `PyPDFLoader`  
- Split large documents into smaller chunks for better retrieval  
- Create embeddings using `sentence-transformers`  
- Store and query embeddings with FAISS vector database  
- Run **local inference** using `llama-cpp-python` with a GGUF model (Mistral-7B-Instruct)  
- Conversational memory support in the Streamlit app  

---

## 📦 Installation

### 1. Clone the repository

git clone <your-repo-url>
cd <repo-folder>

### 2. Create and activate a virtual environment

python -m venv aenv
aenv\Scripts\activate   # On Windows

### 3. Install dependencies

pip install -r requirements.txt
⚠️ Make sure you also have Visual Studio Build Tools 2022 (C++ workload) installed for compiling llama-cpp-python.

## 📂 Project Structure

├── app.py                # Streamlit web app
├── multi_pdf_chat.py     # CLI-based chatbot
├── requirements.txt      # Python dependencies
├── models/               # Place your GGUF model file here
├── data/                 # Store your PDF documents here

## 🧠 Model Setup
Download a GGUF model of Mistral-7B-Instruct (e.g. mistral-7b-instruct-v0.2.Q4_K_M.gguf)
from TheBloke HuggingFace models.

Place it inside the models/ folder.

Update the model_path in your code if needed.

## ▶️ Usage
Run from Command Line

python multi_pdf_chat.py
Type your questions about the PDFs in the terminal.

Type exit to quit.

Run the Streamlit App

streamlit run app.py
Upload PDFs via the sidebar

Ask questions in the chat interface

Get answers powered by Mistral-7B

## 📝 Requirements
Python 3.10+

llama-cpp-python (requires Visual Studio Build Tools on Windows)

Enough RAM/CPU for running Mistral (or GPU if compiled with CUDA)

##📜 License
This project is for educational purposes.
Model weights are subject to their original licenses.
