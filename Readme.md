# 🎥 VidIntel

An AI-powered **YouTube video summarization and question-answering app** built with **Gradio**, **LangChain**, **FAISS**, and **IBM watsonx.ai**.
This application extracts YouTube transcripts, summarizes long videos, and allows users to ask contextual questions grounded strictly in the video content.

---

## 🚀 Features

* 📜 **Automatic YouTube Transcript Extraction**
* ✂️ **Smart Text Chunking** using LangChain splitters
* 🧠 **Semantic Search with FAISS**
* 🧾 **Concise Video Summarization**
* ❓ **Context-aware Question Answering**
* 🔗 **IBM Granite LLM (watsonx.ai)**
* 🌐 **Gradio Web UI**

---

## 🧠 Architecture Overview

```text
YouTube URL
   ↓
Transcript Extraction (youtube-transcript-api)
   ↓
Preprocessing & Chunking (LangChain)
   ↓
Embeddings (IBM Slate-30M)
   ↓
FAISS Vector Store
   ↓
LLM (IBM Granite 3.2)
   ↓
Summary / Q&A Output
```

---

## 🛠️ Tech Stack

| Layer      | Technology                   |
| ---------- | ---------------------------- |
| UI         | Gradio                       |
| LLM        | IBM Granite 3.2 (watsonx.ai) |
| Embeddings | IBM Slate-30M                |
| Framework  | LangChain                    |
| Vector DB  | FAISS                        |
| Transcript | youtube-transcript-api       |
| Language   | Python 3.10+                 |

---

## 📦 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/PRONGS-CHIRAG/Vidintel.git
cd Vidintel
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 IBM watsonx.ai Setup

You **must** have access to **IBM watsonx.ai**.

### Required:

* IBM Cloud Account
* watsonx.ai project
* Project ID

The app currently uses:

```python
project_id = "skills-network"
url = "https://us-south.ml.cloud.ibm.com"
```

> ⚠️ For production use, **store credentials securely using environment variables**.

---

## ▶️ Run the Application

```bash
python app.py
```

Then open:

```
http://localhost:7860
```

---

## 🧪 How to Use

### 🔹 Summarize a Video

1. Paste a YouTube video URL
2. Click **“Summarize Video”**
3. Receive a concise AI-generated summary

### 🔹 Ask Questions

1. Enter a question about the video
2. Click **“Ask a Question”**
3. Get an answer grounded in the transcript

---

## 🧩 Project Structure

```text
.
├── app.py                  # Main Gradio application
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
```

---

## 🧠 Models Used

### LLM

* **ibm/granite-3-2-8b-instruct**

### Embeddings

* **ibm/slate-30m-english-rtrvr-v2**

---

## ⚠️ Known Limitations

* ❌ Works only with videos that have English transcripts
* ❌ Private / restricted videos are not supported
* ⚠️ Transcript fetching depends on YouTube availability
* ⚠️ Cold start latency due to LLM initialization

---

## 🔮 Future Improvements

* ⏱️ Timestamp-aware answers
* 🌍 Multi-language support
* 💾 Persistent vector storage
* 🔄 Streaming responses
* 🔐 Secure credential handling
* 🚀 Deployment on Hugging Face Spaces

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a Pull Request

---

## 📄 License

MIT License
Feel free to use, modify, and distribute.

---

## 🙌 Acknowledgements

* IBM watsonx.ai
* LangChain
* Gradio
* FAISS
* YouTube Transcript API

---

## 📬 Contact

If you’re building **AI, RAG, or agentic systems** and want to collaborate:

**Chirag**
🔗 LinkedIn - https://www.linkedin.com/in/chiragnvijay/
💡 Open to research, startups, and applied AI projects

---

