

# Conversational Q\&A Chatbot

This project is a Conversational Q\&A Chatbot that leverages memory to allow users to engage in multi-turn conversations. It combines language models with retrieval-based capabilities and chat history management.

## 🔧 Technologies Used

* **Python**
* **LangChain** – for chaining LLM and retrieval tools
* **ChatGroq (Llama3-8b-8192)** – for conversational LLM responses
* **HuggingFace Embeddings (`all-MiniLM-L6-v2`)** – for converting text to vector embeddings
* **BeautifulSoup (`bs4`)** – for HTML parsing (installed via pip)
* **dotenv** – for managing API keys securely
* **.env File** – to securely load:

  * `GROQ_API_KEY`
  * `HF_TOKEN`

## 💡 Features

* **Retrieval-Augmented Generation (RAG)**: Uses HuggingFace sentence embeddings to vectorize and retrieve relevant documents.
* **Conversational Memory**: Maintains context across chat interactions.
* **Dual Modes**:

  * **Chains**: Always retrieve context before responding.
  * **Agents**: LLM decides when and how to retrieve.

## 📁 How It Works

1. **Load Environment Variables** using `dotenv`.
2. **Set Up LLM** from Groq (`ChatGroq` with Llama3).
3. **Embed Documents** using HuggingFace Embeddings.
4. **Retrieve Relevant Data** from your vector store.
5. **Chat** with memory context included in every response.

## 🚀 Getting Started

1. Clone the repository or open the `bot.ipynb` notebook.
2. Install dependencies:

   ```bash
   pip install langchain langchain-groq langchain-huggingface bs4 python-dotenv
   ```
3. Add a `.env` file with your API keys:

   ```env
   GROQ_API_KEY=your_groq_api_key
   HF_TOKEN=your_huggingface_token
   ```
4. Run the notebook cells step-by-step to initialize and chat.

---


