🔍 Multimodal RAG Pipeline with LangChain, GROQ, and Web Search Integration
This project implements a Retrieval-Augmented Generation (RAG) system powered by LangChain. It uses hybrid routing between a vector database (Chroma) and web search (Tavily API), backed by GROQ's Gemma2-9b-It LLM to answer user queries with dynamic routing, grading, hallucination detection, and query rewriting capabilities.

🚀 Features
✅ Hybrid Retrieval Routing: Smart routing of queries to vectorstore or web search

🧠 LLM Answer Generation: Uses GROQ’s Gemma2-9b-It model for high-quality generations

📚 Document Retrieval & Relevance Grading: Vector-based and web-based document retrieval with semantic filtering

🕵️‍♀️ Hallucination Detection: Ensures answer grounding with the retrieved sources

📝 Answer Relevance Grading: Evaluates if the LLM response answers the question

🔁 Query Rewriting: Enhances user questions for better semantic matching in vector DB

🌐 Web Search Integration: Powered by Tavily Search API for fresh content retrieval

🧰 Tech Stack
LangChain - for orchestration and chaining

Chroma - vector database for document retrieval

GROQ API - LLM inference (Gemma2-9b-It)

Tavily API - web search engine integration

HuggingFace Embeddings - vector representation of documents

Dotenv - secure API key management

🛠️ Setup
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/multimodal-rag-langchain.git
cd multimodal-rag-langchain
2. Install Dependencies
Make sure you have Python 3.10+ and run:

bash
Copy
Edit
pip install -r requirements.txt
3. Set Environment Variables
Create a .env file in the root with:

env
Copy
Edit
GOOGLE_API_KEY=your_google_key
TAVILY_API_KEY=your_tavily_key
GROQ_API_KEY=your_groq_key
LANGCHAIN_API_KEY=your_langchain_key
📦 How It Works
Initialize API Keys: Loads API keys from .env using dotenv.

Embed Documents: Uses HuggingFace all-MiniLM-L6-v2 embeddings.

Load Web Documents: Loads articles from Lilian Weng’s blog for vectorstore ingestion.

Split & Store Docs: Uses RecursiveCharacterTextSplitter and stores in Chroma.

Question Routing: Routes queries either to vectorstore or Tavily web search.

RAG Chain: Formats prompt, invokes LLM, and generates response.

Grading System: Grades document relevance, hallucination, and answer quality.

Query Rewriting: Improves queries that fail to retrieve relevant content.

🧪 Example
python
Copy
Edit
question = "What are the types of agent memory?"

# Automatically routes the question
# Retrieves relevant documents
# Grades their relevance
# Generates a response with LLM
# Grades hallucination and answer relevance
📂 Directory Structure
bash
Copy
Edit
.
├── main.py
├── .env
├── requirements.txt
└── README.md
✍️ Author
Your Name – @yourhandle

📄 License
This project is licensed under the MIT License.
