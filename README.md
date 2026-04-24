# Agentic RAG System with Human-in-the-Loop (HITL)

## 📌 Project Overview
This project implements an advanced **Retrieval-Augmented Generation (RAG)** system designed for the University of Arkansas Extension. It bridges the gap between automated AI efficiency and human expert reliability. By utilizing **LangGraph**, the system can detect when a query falls outside its knowledge base and pause execution for human intervention, ensuring 100% factual accuracy for customer support.

## 🚀 Key Features
- **Dynamic Retrieval:** Real-time semantic search using ChromaDB to ground LLM responses.
- **Stateful Orchestration:** Managed via LangGraph to handle complex, non-linear workflows.
- **Human-in-the-Loop (HITL):** A manual escalation gateway that triggers an `interrupt` when information is missing.
- **Persistent Checkpointing:** Saves the state of a conversation, allowing it to be resumed after human review.

## 🛠️ Tech Stack
- **Language Model:** Gemini 2.5 Flash
- **Orchestration:** LangGraph & LangChain
- **Vector Database:** ChromaDB
- **Embeddings:** `gemini-embedding-001`
- **Processing:** PyPDFLoader & RecursiveCharacterTextSplitter

## 📂 Project Structure
- `/docs`: Contains HLD, LLD, and Technical Documentation PDFs.
- `/data`: Includes the University of Arkansas Extension policy PDF.
- `/images`: Architecture and Workflow diagrams.
- `requirements.txt`: Python dependencies.
- `Final_Project_Notebook.ipynb`: The complete implementation code.

## ⚙️ Setup & Prerequisites
### Prerequisites
- Python 3.9+
- A Google Cloud API Key (for Gemini)

### Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/VedikaPunjabi/Agentic-RAG-Customer-Support
   cd your-repo-name

2. **Install dependencies:**
    ```bash
    pip install -r requirements.txt

3. **Configure Environment:**
Create a .env file or set your API key:
    ```bash
    export GOOGLE_API_KEY='your_api_key_here'

## 📊 System Architecture
The system operates as a state machine:

1. Start: User input is received.

2. Assistant Node: Retrieves context from the vector store and generates a response.

3. Routing Logic: If the assistant identifies a lack of context, it routes to the human_review node.

4. End: If the response is grounded and verified, it is delivered to the user.

## 🔗 Submission Links
Video Walkthrough: https://drive.google.com/file/d/1q-4MC6Pi2E4_R8NVMih8VnL3Gv_iwUAF/view?usp=sharing

LinkedIn Portfolio: https://www.linkedin.com/posts/punjabi-vedika-2391a73b1_genai-rag-langgraph-activity-7453427302371106816-xtMv?utm_source=share&utm_medium=member_desktop&rcm=ACoAAGSV9o0BRLwHvyI__9O_w_oDyOk2tVBzn-Y

##

**Author: Vedika Punjabi**

**Internship:** Generative AI Intern @ Innomatics Research Labs
