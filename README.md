###### ####### STARTING ###############
# Independent RAG Chatbot using Ollama Bridge
This project demonstrates a robust and cost-effective Retrieval-Augmented Generation (RAG) chatbot solution that entirely bypasses traditional cloud API limitations by utilizing Ollama as a flexible LLM bridge.

The RAG system is designed to provide highly accurate, contextual answers based on your private, local documents (PDFs) and features a clean, professional chat interface built with Gradio.

###### ####### Key Features ##############
# API-Free Generation:
Uses Ollama to connect with powerful models (e.g., gpt-oss:120b-cloud) without the need for traditional commercial API keys or expensive quotas.

# Local Embeddings: 
Leverages the all-MiniLM-L6-v2 model for generating document embeddings entirely on the local machine (CPU), making the data processing step cost-free and private.

# Persistent Vector Store: 
Uses FAISS to save the document embeddings locally, allowing instant restarts without reprocessing the document every time.

# Conversation Memory: 
Maintains chat history within the session using LangChain's ConversationBufferMemory.

# Professional UI: 
A clean, responsive GPT-style chat interface built using Gradio.


###### ####### Project Setup (Prerequisites) #################
Before running the application, ensure you have Python 3.11 installed and Ollama running on your system.
# Ollama Installation & Setup
1. install Ollama from their official website. Once installed, ensure the Ollama server is running in the background.
2. Since you are using a Cloud Model, no local model download is strictly necessary, but the Ollama server must be active to proxy the request.
# Environment and Dependencies
Clone the Repository:
git clone https://github.com/Abdul-Hamidd/ollama-api-free-rag
cd ollama-api-free-rag
# Create Virtual Environment (Recommended):
python -m venv venv
.\venv\Scripts\activate # On Windows
# Install Dependencies: 
Use the requirements.txt file to install necessary libraries.
**pip install -r requirements.txt**
# Place Document:
Place your target PDF document in the main project directory, or update the FILE_PATH variable in the script


###### ############# How to Run #################
The entire RAG pipeline and Gradio interface are typically combined into a single script (e.g rag_building.ipynb).
# Initial RAG Setup (Embeddings)
the script will automatically perform the following steps on the first run:
1. Load the PDF documments.
2. Split the document into chunks.
3. Generate embeddings using all-MiniLM-L6-v2.
4. Create and save the faiss_index_local_rag directory.
# Launch the Chatbot
Execute the main Python script: rag_building.ipynb
A Gradio user interface will automatically open in your browser, and you can start interacting with your RAG system immediately.


###### ################ Author ####################

# Name: Abdul Hmaid
# LinkeDin: https://linkedin.com/in/abdul-hamid786
# Email: hamzahmuhammad750@gmail.com


