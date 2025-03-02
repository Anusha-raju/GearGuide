# 🤖 AI RAG Advisor Chatbot

The **AI RAG Advisor Chatbot** is an intelligent **Retrieval-Augmented Generation (RAG) system** powered by **Neo4j and OpenAI**. It helps users **diagnose issues**, provides **insights** based on a structured knowledge graph, and allows for **multi-turn conversations**.

## 🌟 Features

✅ **Conversational AI** – Supports **multi-turn** chat interactions.  
✅ **Graph-Based Retrieval** – Uses **Neo4j** for structured knowledge retrieval.  
✅ **OpenAI Embeddings** – Enhances search accuracy using **vector similarity**.  
✅ **Interactive UI** – Built with **Streamlit** for an engaging chat experience.  
✅ **Auto-refreshing Chat History** – Ensures **smooth** interactions.  
✅ **Modern UI** – Includes **styled chat bubbles, avatars, and a sidebar.**  

---
# 🤖 AI RAG Advisor Chatbot

The **AI RAG Advisor Chatbot** is an intelligent **Retrieval-Augmented Generation (RAG) system** powered by **Neo4j and OpenAI**. It helps users **diagnose issues**, provides **insights** based on a structured knowledge graph, and allows for **multi-turn conversations**.

## 🌟 Features

✅ **Conversational AI** – Supports **multi-turn** chat interactions.  
✅ **Graph-Based Retrieval** – Uses **Neo4j** for structured knowledge retrieval.  
✅ **OpenAI Embeddings** – Enhances search accuracy using **vector similarity**.  
✅ **Interactive UI** – Built with **Streamlit** for an engaging chat experience.  
✅ **Auto-refreshing Chat History** – Ensures **smooth** interactions.  
✅ **Modern UI** – Includes **styled chat bubbles, avatars, and a sidebar.**  

---

## 🚀 Installation & Setup

### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/yourusername/ai-rag-advisor.git
cd ai-rag-advisor
```

### **2️⃣ Create a Virtual Environment**
```sh
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate  # Windows
```

### **3️⃣ Install Dependencies**
```sh
pip install -r requirements.txt
```

### **4️⃣ Set Up Environment Variables**
Create a `.env` file in the project root and add the following:
```ini
NEO_URI="bolt://localhost:7687"  # Update if using a remote Neo4j instance
NEO_USERNAME="neo4j"
NEO4J_PASSWORD="your_password"
OPENAI_API_KEY="your_openai_api_key"
```

### **5️⃣ Start Neo4j**
Ensure Neo4j is running:
```sh
neo4j console
```

### **6️⃣ Run the Chatbot**
```sh
streamlit run streamlit_ui.py
```

---

## 🛠️ Usage

1. Open the **Streamlit UI** in your browser.
2. Type a query in the chat input box.
3. The chatbot retrieves relevant information from **Neo4j**.
4. Continue the conversation – previous context is remembered!
5. Click **"Clear Chat"** to start a new conversation.

---

## 📀 System Architecture

### **1️⃣ Data Ingestion**
- Parses structured **XML** files.
- Cleans data and stores it in **Neo4j** as a **Knowledge Graph**.
- Creates **vector embeddings** for each entity.

### **2️⃣ Vector Search & Retrieval**
- Uses **OpenAI embeddings** (`text-embedding-3-small`).
- Performs **vector similarity search** in Neo4j.
- Retrieves **top-K relevant nodes**.

### **3️⃣ Multi-Turn Conversational Logic**
- Maintains **chat history** for contextual conversations.
- Uses **re-ranking** to improve responses.
- Retrieves **parent-child relationships** for deeper insights.

---

## 🔖 Example Query & Response

### **User:** "Why is my car engine making noise?"
### **Bot:** 
```
It could be due to worn-out belts or misfiring cylinders.
Do you notice any vibrations?
```

### **User:** "Yes, I feel vibrations when accelerating."
### **Bot:** 
```
This might indicate an issue with the engine mounts or transmission.
Would you like diagnostic steps?
```

---

## 📉 Technologies Used

| Tech      | Purpose |
|-----------|----------------------|
| **Python** | Core language |
| **Streamlit** | Interactive UI |
| **Neo4j** | Knowledge Graph Storage |
| **OpenAI** | AI-based embeddings |
| **Pandas** | Data Processing |
| **dotenv** | Environment Management |

---

## 📂 File Structure

```plaintext
📂 ai-rag-advisor
│── 📂 data_ingestion         # Data parsing & insertion into Neo4j
│── 📂 embeddings             # OpenAI embedding generation
│── 📂 retrieval              # Vector similarity search logic
│── 📂 ui                     # Streamlit UI for chatbot
│── 📄 app.py                 # Main chatbot logic
│── 📄 streamlit_ui.py        # Streamlit interface
│── 📄 requirements.txt       # Dependencies
│── 📄 .env                   # API keys & DB credentials
│── 📄 README.md              # Project documentation
```

---

## 🤝 Contributing

💡 Have suggestions or improvements? Feel free to submit a **Pull Request**!

1. Fork the repository.
2. Create a new branch (`feature-new-idea`).
3. Commit your changes and push.
4. Submit a **PR**!

---

## 🛠️ Troubleshooting

### **Neo4j Connection Errors**
💪 Ensure Neo4j is **running** before launching the chatbot.  
💪 Verify credentials in the **.env file**.  
💪 Run this command to test the connection:
```sh
cypher-shell -u neo4j -p your_password
```

### **OpenAI API Errors**
💪 Ensure your **API key** is valid (`OPENAI_API_KEY`).  
💪 Check your **API rate limits** on [OpenAI's platform](https://platform.openai.com).  

---

## 📜 License

This project is **MIT Licensed**. Feel free to modify and distribute it! 🚀

---

## �
