### README for Chat PDF Application

---

# Chat PDF 💬📚

Chat PDF is a Streamlit-based web application that allows users to upload PDF files and ask questions about their content. The application leverages Google's Gemini API for embeddings and conversational AI to provide precise and contextual answers based on the uploaded PDF documents.

---

## Features

- Upload multiple PDF files for processing.
- Extract text from PDF files.
- Split text into manageable chunks for efficient querying.
- Vectorize text chunks using Google Gemini embeddings.
- Store and persist embeddings using Chroma.
- Answer user questions based on the context extracted from PDF files.

---

## Requirements

### Python Libraries

The following Python libraries are required:

- `streamlit`
- `PyPDF2`
- `langchain`
- `langchain-google-genai`
- `google-generativeai`
- `dotenv`
- `chromadb`

### Environment Variables

The application uses the `GOOGLE_API_KEY` to connect to the Google Gemini API. You need to set up a `.env` file in the root directory with the following content:

```plaintext
GOOGLE_API_KEY=your_google_api_key
```

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/chat-pdf.git
cd chat-pdf
```

### 2. Set up a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # For Linux/macOS
venv\Scripts\activate     # For Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

Create a `.env` file in the project directory and add your Google API key:

```plaintext
GOOGLE_API_KEY=your_google_api_key
```

---

## Usage

### Run the Application

Start the Streamlit app by running:

```bash
streamlit run app.py
```

### Steps to Use

1. **Upload PDFs**: Use the sidebar to upload one or more PDF files.
2. **Process Files**: Click the "Submit & Process" button to extract and vectorize text from the uploaded PDFs.
3. **Ask Questions**: Type your question in the input box on the main page, and the app will provide an answer based on the processed content.

---

## File Structure

```
chat-pdf/
├── chroma_db/           # Directory where vectorized embeddings are stored
├── app.py               # Main application file
├── requirements.txt     # Python dependencies
├── .env                 # Environment variables
└── README.md            # Documentation
```

---

## Example

1. **Uploading PDFs:**
   - Drag and drop or select files using the file uploader in the sidebar.

2. **Processing PDFs:**
   - Once uploaded, click **Submit & Process** to extract and vectorize content.

3. **Asking Questions:**
   - Enter a question like: *"What is the summary of Chapter 2?"* in the input box, and the application will reply.

---

## Limitations

- The application relies on Google's Gemini embeddings and may require internet access to function.
- Processing large PDFs with extensive content might take additional time.
- Responses are limited to the context present in the uploaded PDFs.

---

## Contributing

Contributions are welcome! Feel free to submit issues or pull requests to enhance functionality or improve documentation.

---------
