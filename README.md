# 📑 Ollama-Bridge RAG Chatbot: Local Persistent Vector Architecture with Gradio UI

A production-ready, highly cost-effective **Retrieval-Augmented Generation (RAG)** chatbot solution designed to deliver hyper-localized contextual intelligence over private PDF documents. By utilizing **Ollama as an isolated local LLM orchestration bridge**, this architecture completely eliminates dependency on external commercial cloud APIs, ensuring absolute data privacy, zero token costs, and offline compute capabilities.

---

## 🧠 System Architecture & Data Pipeline

The pipeline implements an offline-first data ingestion and retrieval workflow, isolating document splitting, vector serialization, and generation layers:

<p align="center">
  <img src="https://github.com/Abdul-Hamidd/ollama-api-free-rag-chatbot/raw/main/RAG%20Architecture%20Diagram.png" alt="RAG Chatbot Visual Workflow Diagram" width="850">
</p>

## 🚀 Core Technical Features

* **API-Free Local Orchestration:** Interfaces directly with localized weights using Ollama, removing traditional rate limits, pay-as-you-go commercial billing traps, and latency spikes.
* **Cost-Free Embedding Compute:** Leverages the open-source `all-MiniLM-L6-v2` sentence-transformer model to map semantic embeddings completely on local CPU resources.
* **Persistent Index Virtualization:** Uses a highly-optimized FAISS (Facebook AI Similarity Search) local directory structure to cache vector indexes, avoiding redundant reprocessing overhead across system reboots.
* **Conversational Memory Buffering:** Features LangChain's native `ConversationBufferMemory` state management to retain multi-turn interaction history within an active session.
* **Sleek GPT-Style Frontend:** Features a web-responsive, streamlined chatbot layout powered natively by Gradio for clean multi-turn presentation.

---

## ⚙️ Core Stack & Dependency Frameworks

* **Orchestration Matrix:** LangChain Core, LangChain Community
* **Vector Mechanics:** FAISS (CPU variant), HuggingFace Transformers
* **Generative Engine:** Ollama Client Runtime
* **Interface Management:** Gradio UI Components
* **Document Processing:** PyPDF Data Utilities

---

## 🛠️ Workspace Provisioning & Installation

### 1. System Requirement Dependencies
Before setup, download and configure the background daemon for **Ollama** from the official platform. Once installed, download your target inference weights via terminal:
```bash
ollama pull llama3
2. Repository Infrastructure Clone
Bash
git clone [https://github.com/Abdul-Hamidd/ollama-api-free-rag-chatbot.git](https://github.com/Abdul-Hamidd/ollama-api-free-rag-chatbot.git)
cd ollama-api-free-rag-chatbot
3. Isolated Virtual Environment Build
Bash
# Environment Creation
python -m venv venv

# Activation (Windows Native PowerShell)
.\venv\Scripts\activate

# Activation (Linux / macOS Shell)
source venv/bin/activate
4. Dependency Resolution
Bash
pip install -r requirements.txt
5. Document Placement Ingestion
Drop your corporate or personal targeted documentation files (PDF format) straight into the root working directory of this project space.

▶️ Pipeline Execution & Deployment
Run the System via Native Script
To run the end-to-end RAG workflow (which automatically processes documentation chunks on the initial launch and instantiates the server backend):

Bash
python app.py
(Note: If utilizing the experimental interactive runtime workspace, execute all localized workbook blocks sequentially inside rag_building.ipynb)

Upon successful binding, a localized host address loopback link (e.g., http://127.0.0.1:7860) will automatically output to your terminal console interface. Click to launch the web client immediately.

🧪 Pipeline Stage Blueprint
Document Loading: LangChain ingestion streams scrape raw textual elements from local path indicators.

Granular Index Partitioning: Documents are broken down into dense target tokens with overlap thresholds to guarantee zero loss of context over sentence seams.

FAISS Serialization Cache: Vector blocks are mapped onto localized disk infrastructure under the directory tag /faiss_index_local_rag.

Augmented Synthesis Prompt: Similarity matching indexes top-tier data fragments and directly attaches them to the user prompt layout before triggering model generation.

🌟 Strategic Project Roadmap
[ ] Integrate hybrid keyword-sparse rankers (BM25) alongside dense FAISS vectors for absolute retrieval accuracy.

[ ] Build multi-file schema management capabilities to upload disparate formats (.txt, .docx, .json) concurrently via the UI.

[ ] Dockerize the environment tree layout to establish single-click background service setups across cloud or hybrid servers.

👨‍💻 Developer Architecture Profile
ABDUL HAMID GenAI & AI/ML Engineer linkedin.com/in/abdul-hamid786 | wellfound.com/u/abdul-hamid-29 | https://www.kaggle.com/hamidai

Give this repository a star ⭐ if you find this local offline RAG architecture implementation helpful for enterprise compliance workflows!
