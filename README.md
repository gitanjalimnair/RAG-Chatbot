# 🤖 RAG Chatbot with Gemini & FAISS

A Retrieval-Augmented Generation (RAG) chatbot that allows users to upload PDF documents and ask natural language questions about their contents. The application uses Google's Gemini Embedding Model to generate embeddings, FAISS for efficient vector similarity search, and Gemini Pro for answer generation.

## 🌐 Live Demo

🔗 https://rag-pdf05.streamlit.app/
## 🚀 Features

- 📄 Upload PDF documents
- ✂️ Automatically extract and split text into chunks
- 🧠 Generate embeddings using Google Gemini
- 🔍 Store and retrieve embeddings with FAISS
- 💬 Ask questions in natural language
- 📚 Display the retrieved context used to generate answers
- 🌐 Interactive Streamlit web interface

---

## 🛠️ Tech Stack

- **Python**
- **Streamlit**
- **LangChain**
- **Google Gemini API**
- **FAISS**
- **PyPDF**
- **Python Dotenv**

---

## 📂 Project Structure

```
RAG-Chatbot/
│
├── app.py                  # Streamlit application
├── ingest.py               # Creates FAISS vector database
├── rag.py                  # Handles retrieval and question answering
├── utils.py                # PDF extraction and text chunking
├── requirements.txt
├── README.md
│
├── uploads/                # Uploaded PDFs
├── vectorstore/            # Generated FAISS index
│
└── .env                    # API key (not included in repository)
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/RAG-Chatbot.git
cd RAG-Chatbot
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it:

**Windows**

```bash
.venv\Scripts\activate
```

**Linux/macOS**

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root.

```env
GOOGLE_API_KEY=YOUR_API_KEY
```

Alternatively, when deploying on Streamlit Cloud, add the API key under **App Settings → Secrets**:

```toml
GOOGLE_API_KEY="YOUR_API_KEY"
```

---

## ▶️ Running the Application

```bash
streamlit run app.py
```

The application will open automatically in your browser.

---

## 📖 How It Works

1. Upload a PDF document.
2. Text is extracted using **PyPDF**.
3. The extracted text is divided into smaller chunks.
4. Gemini generates embeddings for each chunk.
5. Embeddings are stored in a FAISS vector database.
6. When a question is asked:
   - The query is embedded.
   - FAISS retrieves the most relevant chunks.
   - Gemini generates an answer using the retrieved context.

---

## 📸 Demo

<img width="1917" height="1020" alt="image" src="https://github.com/user-attachments/assets/ad773694-7f16-43fe-a415-448281b7349a" />
<img width="1917" height="1017" alt="image" src="https://github.com/user-attachments/assets/ce41c6d9-e12d-47f7-bc79-434e807dbdb9" />



---

## Future Improvements

- Support multiple PDFs
- Chat history
- Source page references
- Export conversations
- Additional document formats (DOCX, TXT)

---

## 👨‍💻 Author

**Gitanjali M. Nair**

GitHub: https://github.com/YOUR_USERNAME

---

## 📄 License

This project is intended for educational and learning purposes.
