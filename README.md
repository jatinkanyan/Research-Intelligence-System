# Research-Intelligence-System
An AI-powered system for analyzing academic research papers. Users can upload PDFs to generate concise summaries, structured insights, and ask context-aware questions using LLMs and semantic search. Built with Streamlit, LangChain, FAISS, and Groq LLaMA models.
📚 Research Intelligence System

An end-to-end AI-powered research paper analysis system that allows users to upload academic PDFs and interact with them using summarization, semantic search, and question answering.
Built with Python, LangChain, Groq LLMs, FAISS, and Streamlit.

🚀 Features

📄 PDF Ingestion

Extracts text from research papers using pdfplumber

Preserves page-level context for accurate referencing

✂️ Smart Chunking

Splits large documents into manageable, overlapping chunks

Enables efficient embedding and retrieval

🧠 Semantic Search & QA

Uses vector embeddings + FAISS for similarity search

Ask natural-language questions about the paper

📝 LLM-Based Summarization

Short summary of the paper

Structured summary (objective, methodology, findings, conclusion)

🖥️ Interactive Streamlit UI

Upload PDFs

Ask questions

Get answers grounded in document content

🛠️ Tech Stack
Component	Technology
Language	Python 3.10
UI	Streamlit
PDF Parsing	pdfplumber
LLM	Groq (LLaMA-3.1-8B)
Framework	LangChain
Vector DB	FAISS
Embeddings	Sentence Transformers
📂 Project Structure
Research_intelligence_system/
│
├── backend/
│   ├── ingestion/
│   │   ├── pdf_loader.py
│   │   └── paper_ingestor.py
│   │
│   ├── indexing/
│   │   ├── chunk_builder.py
│   │   └── vector_store.py
│   │
│   ├── summarization/
│   │   ├── paper_summarizer.py
│   │   └── test_summarizer.py
│   │
│   └── qa/
│       └── qa_pipeline.py
│
├── frontend/
│   └── app/
│       └── streamlit_app.py
│
├── venv/
├── requirements.txt
└── README.md

⚙️ Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/your-username/research-intelligence-system.git
cd research-intelligence-system

2️⃣ Create & Activate Virtual Environment
python -m venv venv


Windows

venv\Scripts\activate


Mac/Linux

source venv/bin/activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Set Environment Variables

Create a .env file in the root directory:

GROQ_API_KEY=your_groq_api_key_here

▶️ Run the Application
python -m streamlit run frontend/app/streamlit_app.py


Then open your browser at:

http://localhost:8501

🧪 Testing (Optional)

To test summarization independently:

python -m backend.summarization.test_summarizer

🧠 How It Works

User uploads a PDF

Text is extracted page-wise

Document is chunked intelligently

Chunks are embedded and stored in FAISS

User asks a question

Relevant chunks are retrieved

LLM generates an answer grounded in document context

📌 Key Challenges Solved

✅ Token overflow using chunk-based summarization

✅ Large PDF handling

✅ Modular backend architecture

✅ Streamlit caching for performance

🔮 Future Enhancements

🔍 Highlight answer source pages

📊 Paper comparison feature

🧾 Citation-aware answers

☁️ Cloud deployment

📑 Multi-document support

👨‍💻 Author

Jatin Kanyan
Aspiring Data Scientist | ML & GenAI Enthusiast

📎 Video Link : https://drive.google.com/file/d/19Ss2O0dE9BbGThm0cau7D-nVXMTYXgmV/view?usp=sharing
📎 GitHub: https://github.com/jatinkanyan/Research-Intelligence-System

⭐ If you like this project

Give it a ⭐ on GitHub — it really helps!
