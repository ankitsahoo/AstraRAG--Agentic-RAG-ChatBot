# AstraRAG--Agentic-RAG-ChatBot
- AstraRAG — Agentic RAG Chatbot is an intelligent Retrieval-Augmented Generation (RAG) system powered by autonomous agents and LLMs to provide contextually aware, multi-step reasoning answers.
- It combines CrewAI, LlamaIndex, and Groq LLMs to create a chatbot that can understand queries, retrieve relevant knowledge, and generate high-quality responses based on your custom document data.
- Unlike standard chatbots, AstraRAG leverages Agentic workflows — allowing multiple agents to collaborate, plan, and reason dynamically before producing an answer.
- Built with FastAPI for backend orchestration and Streamlit for an interactive UI, the system is fully containerized using Docker and ready for cloud deployment on AWS EC2.

# ✨Key Highlights

- 🧩 Agentic Intelligence: Powered by CrewAI agents for reasoning and decision-making.
- 🔍 RAG Pipeline: Uses LlamaIndex + ChromaDB for context-based retrieval from your knowledge base.
- ⚡ High-speed LLMs: Integrated with Groq API running Llama 3.3 70B for fast inference.
- 🖥️ Modern Stack: FastAPI backend + Streamlit frontend for a seamless developer & user experience.
- ☁️ Scalable Deployment: Fully containerized with Docker, deployable on AWS EC2 or any cloud service.

# Tech Stack I used
- **CrewAI**- will be powering my agents enabling mutlistep aware and context reasoning.
- **FastAPI**- Used in backend will send request and orchestrate the workflow.
- **StreamLit**- used as User Interface
- **Groq**- LLM Provider 
-**Model Used**- llama3.3:70b (42gb)
- **ChromaDB**- Used as vectorstore to manage embeddings and retreival.
- **LlamaIndex**- It will provide the RAG pipline to connect chabot with external Knowledge.
- **Docker**- To containrize the application
- **AWS EC2**- For Deployment

# flowchart

- 🧑User interacts with 🌐Streamlit UI and submits a query.
- ⚡FastAPI receives it and forwards the task to a 🧠CrewAI Agent.
- The CrewAI Agent triggers the RAG Tool powered by 📚 LlamaIndex and 🗄️ChromaDB.
- The RAG pipeline retrieves relevant documents and sends them with the query to Groq (🤖Llama 3.3 70B) for -reasoning.
- The LLM generates a grounded response, which flows back to the frontend via FastAPI.
- The app is containerized with Docker and deployed on AWS EC2 for production access.

Here’s the query-response workflow:

| Step | Component                                | Action                                                                                     |
| ---- | ---------------------------------------- | ------------------------------------------------------------------------------------------ |
| 1    | 🧑 User                                   | Enters query →                                                                              |
| 2    | 🌐 Streamlit UI                           | Sends request to backend →                                                                  |
| 3    | ⚡ FastAPI Backend                         | Orchestrates workflow and forwards to CrewAI →                                              |
| 4    | 🧠 CrewAI Agent                           | Performs reasoning and multi-step task execution →                                         |
| 5    | 📚 RAG Tool (LlamaIndex + 🗄️ ChromaDB)  | Retrieves relevant documents from vector store →                                           |
| 6    | 🤖 Groq LLM API (Llama 3.3 70B)          | Generates grounded, context-aware answer →                                                 |
| 7    | 🔄 Response Flow                          | Answer returned: RAG Tool → CrewAI → FastAPI → Streamlit →                                  |
| 8    | 🌐 Streamlit UI                           | Displays the final answer to the user                                                      |
                                                   |

# ⚙️AstraRAG Complete Workflow Overview

### Query & Response Workflow

🧑 **User**  
&nbsp;&nbsp;↓  
🌐 **Streamlit UI** – Sends request to backend  
&nbsp;&nbsp;↓  
⚡ **FastAPI Backend** – Orchestrates workflow and forwards to CrewAI  
&nbsp;&nbsp;↓  
🧠 **CrewAI Agent** – Performs multi-step reasoning  
&nbsp;&nbsp;↓  
📚 **RAG Tool (LlamaIndex + 🗄️ ChromaDB)** – Retrieves relevant documents  
&nbsp;&nbsp;↓  
🤖 **Groq LLM API (Llama 3.3 70B)** – Generates context-aware answer  
&nbsp;&nbsp;↑  
🔄 **Response Flow** – Answer returned: RAG → CrewAI → FastAPI → Streamlit UI  
&nbsp;&nbsp;↓  
🌐 **Streamlit UI** – Displays final answer

# 🧱 Deployment Flow

         +---------------------------------------------------------+
         | 🖥️ App Components: 🌐 Streamlit + ⚡ FastAPI + 🧠 CrewAI  |
         |             + 📚 LlamaIndex + 🗄️ ChromaDB               |
         +---------------------------------------------------------+
                              │
                              ▼
         +-------------------------------+
         | 🐳 Docker Container           |
         | (Containerized environment)  |
         +-------------------------------+
                              │
                              ▼
         +-------------------------------+
         | ☁️ AWS EC2 Instance           |
         | (Production deployment)      |
         +-------------------------------+
                              │
                              ▼
         +-------------------------------+
         | 🌐 Public Access               |
         | (Users interact with chatbot) |
         +-------------------------------+


##### Some Screenshot related to Agentic RAG how it is retriving the answers to the Users query #######

**VectorDB creation**
![alt text](<Screenshot (29).png>)

**Agentic RAG Response**
![alt text](<Screenshot (30).png>) 
![alt text](<Screenshot (31).png>) 
![alt text](<Screenshot (32).png>)

# After integrating both frontend and backend 

**Frontend**
![alt text](<Screenshot (34).png>)

**In backend how agent is executing**
![alt text](<Screenshot (33).png>)

![alt text](<Screenshot (36).png>)

# Deployment ScreenShots

**Build the Docker Image of the AstraRAG**

# 🐳 Docker Image Details

| **Repository**     | **Tag**  | **Image ID**   | **Created**       | **Size**  |
|--------------------|----------|----------------|-------------------|-----------|
| astrarag-chatbot   | latest   | 34186c7d8610   | 14 minutes ago    | 13.7 GB   |

![alt text](<Screenshot (37).png>)

# ⚙️ Deployed the application to AWS EC2

![alt text](<Screenshot (38).png>)


