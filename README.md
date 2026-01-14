# Research-Intelligence-System

An AI-powered system for analyzing academic research papers. Users can upload PDFs to generate concise summaries, structured insights, and ask context-aware questions using LLMs and semantic search. Built with Streamlit, Groq LLaMA models, FAISS, and custom verification pipelines.

## 📚 Research Intelligence System

An end-to-end AI-powered research paper analysis system that allows users to upload academic PDFs and interact with them using summarization, semantic search, and question answering. 
Built with Python, Groq LLMs, FAISS, and Streamlit.

## 🚀 Features

### 📄 PDF Ingestion
* Extracts text from research papers using `pdfplumber`.
* Preserves page-level context for accurate referencing.

### ✂️ Smart Chunking
* Splits large documents into manageable, overlapping chunks.
* Enables efficient embedding and retrieval via FAISS.

### 🧠 Semantic Search & QA
* Uses vector embeddings + FAISS for similarity search.
* Ask natural-language questions about the paper.
* **Hallucination Detection**: Includes a verification pipeline that fact-checks LLM responses against document evidence.

### 📝 LLM-Based Summarization
* **Short summary**: Quick overview of the paper.
* **Structured summary**: Detailed extraction of Problem Statement, Approach, Contributions, and Results.

### 🕸️ Citation Tracking
* Parses bibliographies to extract cited paper titles and authors.
* Integrates MCP-style tools to lookup external impact metrics and citation counts.

### 🖥️ Interactive Streamlit UI
* **Tabbed Interface**: Switch between Auto-Summary, Research Chat, and Citation Network.
* **Visual Feedback**: Real-time status for indexing and verification checks.

## 🛠️ Tech Stack
| Component | Technology |
| :--- | :--- |
| **Language** | Python 3.10 |
| **UI** | Streamlit |
| **PDF Parsing** | pdfplumber |
| **LLM** | Groq (LLaMA-3.1-8B) |
| **Vector DB** | FAISS |
| **Embeddings** | Sentence Transformers |

## 📂 Project Structure
```text
Research_intelligence_system/
│
├── backend/
│   ├── ingestion/         # paper_ingestor.py, pdf_loader.py
│   ├── indexing/          # chunk_builder.py, faiss_index.py
│   ├── rag/               # qa_pipeline.py, verification.py
│   ├── citation/          # citation_graph.py
│   ├── llm/               # groq_client.py
│   └── models/            # section.py
│
├── frontend/
│   └── app/
│       └── streamlit_app.py
│
├── faiss_store/           # Saved vector indexes
├── uploads/               # Processed PDF storage
├── requirements.txt
└── README.md
⚙️ Installation & Setup
1️⃣ Clone the Repository
Bash

git clone [https://github.com/jatinkanyan/Research-Intelligence-System.git](https://github.com/jatinkanyan/Research-Intelligence-System.git)
cd research-intelligence-system
2️⃣ Create & Activate Virtual Environment
Bash

python -m venv venv
Windows: venv\Scripts\activate

Mac/Linux: source venv/bin/activate

3️⃣ Install Dependencies
Bash

pip install -r requirements.txt
4️⃣ Set Environment Variables
Create a .env file in the root directory:

Code snippet

GROQ_API_KEY=your_groq_api_key_here
▶️ Run the Application
Bash

python -m streamlit run frontend/app/streamlit_app.py
Open your browser at: http://localhost:8501

🧠 How It Works
Upload: User uploads a PDF; text is extracted page-wise.

Index: Document is chunked and stored in a FAISS vector database.

Analyze: User selects between Summary or Chat modes.

Verify: For every answer, a verification step checks the response against retrieved chunks to ensure zero-hallucination.

Connect: References are parsed to build a citation network.

📌 Key Challenges Solved
✅ Hallucination Prevention: Implementation of a "Critic" model to verify LLM claims.

✅ Token Management: Smart slicing of documents for summarization tasks.

✅ Metadata Accuracy: Tracking section headers and page numbers across chunks.

👨‍💻 Author
Jatin Kanyan Aspiring Data Scientist | ML & GenAI Enthusiast

📎 Video Link: Watch Demo 📎 GitHub: jatinkanyan

⭐ If you like this project, give it a ⭐ on GitHub — it really helps!
