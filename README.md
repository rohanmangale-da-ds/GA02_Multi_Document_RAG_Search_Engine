🎥 Recording url - 
📩 Gmail - rohanmangale4001@gmail.com

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 🤖 Multi-Document RAG Chatbot

An AI-powered Research Assistant that allows users to upload documents and interact with them using Retrieval-Augmented Generation (RAG).
It combines LLMs + vector search + optional web search to provide accurate, contextual, and explainable answers.

 
## 📸 SCREENSHOTS - 
### 1. User Interface (UI)
<img width="1915" height="965" alt="image" src="https://github.com/user-attachments/assets/95b27e0d-464b-4038-b9b9-bc13516b60be" />

### 2. Getting required info from document
<img width="1911" height="964" alt="image" src="https://github.com/user-attachments/assets/877b2ea8-90f2-461e-9c24-f0ff6b80172d" />

### 3. Using Web Search When Information Is Not Available in Documents
<img width="1915" height="962" alt="image" src="https://github.com/user-attachments/assets/932337fb-0d0f-4bf0-9e0a-b12448231923" />


### ✨ Key Features

1. Upload and analyze multiple documents (PDF / TXT)
2. Ask natural language questions over your documents
3. Uses RAG (Retrieval-Augmented Generation)
4. Optional Web Search (Tavily) integration
5. Clean & modern Streamlit UI
6. Modular, scalable architecture
7. Built for research, legal, academic, and enterprise use cases

### 💡 Tech Stack

1. UI                -> 	Streamlit
2. LLM	              ->  Groq (LLaMA 3.3 70b)
3. Embeddings        ->	HuggingFace (sentence-transformers)
4. Vector DB	        ->  FAISS
5. Web Search	      ->  Tavily API
6. Backend	          ->  Python
7. Config Management	->  .env, settings.py
8. Architecture	    ->  Modular + Clean


### 📁 Project Structure
```
GA02_Multi_Document_RAG_Search_Engine/
│
├── .streamlit/
│   └── config.toml              # UI theme configuration
│
├── config/
│   ├── __init__.py
│   └── settings.py              # Centralized configuration
│
├── core/
│   ├── chain.py                 # RAG pipeline logic
│   ├── document_processor.py    # Document parsing & chunking
│   ├── embeddings.py            # Embedding generation
│   └── vector_store.py          # FAISS vector store
│
├── tools/
│   └── tavily_search.py         # Web search integration
│
├── ui/
│   ├── chat_interface.py        # Chat UI logic
│   └── components.py            # Reusable UI components
│
├── data/
│   └── input_data/              # Uploaded PDFs
│
├── app.py                       # Streamlit entry point
├── main.py                      # CLI entry (optional)
├── requirements.txt
├── pyproject.toml
├── .env                         # Environment variables (ignored)
├── .gitignore
└── README.md
```

### ⚙️ How It Works (High Level)
#### 1. Document Upload

Users upload PDF or text documents.

#### 2. Chunking & Embedding

Documents are:

Split into meaningful chunks

Converted into embeddings using sentence-transformers

#### 3. Vector Storage

Embeddings are stored in a FAISS vector database for fast similarity search.

#### 4. Query Processing

When a user asks a question:

Relevant chunks are retrieved

Context is injected into the LLM prompt

AI generates a grounded response

#### 5. Optional Web Search

If enabled:

Tavily fetches fresh web data

Results are merged with local document context

### 🖥️ Running the App Locally
1️⃣ Clone the repo
git clone https://github.com/rohanmangale-da-ds/GA02_Multi_Document_RAG_Search_Engine.git
cd GA02_Multi_Document_RAG_Search_Engine

2️⃣ Create virtual environment
python -m venv .venv
source .venv/bin/activate   # Mac/Linux
# OR
.venv\Scripts\activate      # Windows

3️⃣ Install dependencies
pip install -r requirements.txt

4️⃣ Create .env file
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key


⚠️ Do NOT commit .env to GitHub.

5️⃣ Run the app
streamlit run app.py

### 🎨 UI Preview

✔ Chat-style interface
✔ Dark mode friendly
✔ Document upload panel
✔ Optional web search
✔ Real-time responses

### 🧠 Configuration

All configuration lives in:

config/settings.py


Supports:

Environment variables

.env

Streamlit secrets

### 🛡️ Security

No API keys stored in code

.env is ignored

Keys loaded securely at runtime

### 🧪 Example Use Cases

📄 Research paper Q&A

⚖️ Legal document analysis

🧠 Knowledge base assistant

📚 Academic research

🧪 Internal enterprise search
