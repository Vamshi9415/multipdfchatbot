# multipdfchatbot

Sure! Here’s a README.md file for your multipdfchatbot project based on the code in ex.py:

---

# multipdfchatbot

Interactively chat with the contents of your PDF files using Google Gemini (via LangChain) and FAISS vector search, all in a Streamlit app.

## Features

- Upload one or multiple PDF files
- Extracts and indexes PDF content using Google Gemini embeddings
- Asks questions and receives detailed answers based on your uploaded PDFs—answers are contextually grounded
- Simple Streamlit web interface

## Requirements

- Python 3.8+
- Google API Key (for Gemini)
- Streamlit
- PyPDF2
- langchain, langchain-google-genai
- faiss, FAISS Python bindings
- python-dotenv

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Vamshi9415/multipdfchatbot.git
   cd multipdfchatbot
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your environment**
   - Create a `.env` file in the project root:
     ```
     GOOGLE_API_KEY=your-google-api-key-here
     ```

## Usage

1. **Run the Streamlit app**
   ```bash
   streamlit run ex.py
   ```

2. **On the web UI:**
   - Use the sidebar to upload your PDF files
   - Click "Submit & Process" to process and index your PDFs
   - Type your question in the input box and get answers based on your PDF content

## How it Works

- PDFs are parsed and split into manageable text chunks
- Chunks are embedded using Google Gemini Embeddings
- Chunks are indexed by FAISS for efficient similarity search
- User questions are matched to relevant PDF content and answered via Google Gemini (LangChain chain)
- Answers are only given if found in your PDF context

## Notes

- Google Gemini API key is required for embeddings and chat
- Only answers grounded in your PDFs are provided—if the answer is not in the context, the bot will say so
- For best results, use clear and direct questions
