# Streamlit PDF Chat Application

This project is a Streamlit web application that allows users to upload PDF files and ask questions based on the content of those PDFs. The app utilizes Google Generative AI for text embeddings, FAISS for vector storage, and LangChain for handling the conversational chain.

## Features

- **Upload Multiple PDFs**: Users can upload multiple PDF files.
- **Text Extraction**: Extracts text from uploaded PDFs.
- **Text Chunking**: Splits the extracted text into chunks for efficient processing.
- **Vector Store Creation**: Uses FAISS to create a vector store for the text chunks.
- **Conversational AI**: Answers user queries based on the content of the uploaded PDFs using Google Generative AI.
- **Real-Time Interaction**: Provides real-time responses to user queries.

## Installation

### Prerequisites

- Python 3.8 or higher
- Docker (optional but recommended for deployment)
- A Google API key for Generative AI

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/langchain-gemini-Chat-PDFs.git
   cd langchain-gemini-Chat-PDFs

2. **Create a virtual environment**:

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

3. **Install the dependencies**:
pip install -r requirements.txt

4. **Set up environment variables**:
Create a .env file in the root of the project and add your Google API key:
GOOGLE_API_KEY=your-google-api-key

5. **Run the application**:
streamlit run app.py

6. **Docker (Optional)**:
Build and run the application using Docker:
docker build -t my-streamlit-app .
docker run -p 8501:8501 my-streamlit-app

**Usage**
Upload PDFs: Use the sidebar to upload your PDF files.
Process PDFs: Click on the "Submit & Process" button to extract and process the text.
Ask Questions: Type your question in the input box and receive answers based on the PDF content.

**Project Structure**

├── app.py               # Main Streamlit application
├── Dockerfile           # Docker configuration file
├── .gitignore           # Git ignore file
├── requirements.txt     # Python dependencies
├── .env                 # Environment variables (not included in the repo)
├── venv/                # Python virtual environment (excluded from Git)
└── README.md            # Project documentation

**Known Issues**
Network Interruption: Occasionally, network issues might cause connection problems.
WSL Errors: On Windows, Docker might have issues with WSL. Ensure WSL2 is correctly configured.
Contributing

Feel free to submit issues or pull requests. Contributions are welcome!