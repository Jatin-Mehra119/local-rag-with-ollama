
# PDF-Insight PRO offline: Document-Based Offline Question Answering with Ollama 3.1

## Overview

**PDF-Insight PRO offline** is an offline app designed for processing and extracting answers from PDF documents using the Ollama 3.1 LLM. The app runs the model locally, allowing for secure and private data handling. The application leverages text embeddings to index document contents and uses a combination of Chroma for vector storage and similarity-based retrieval for efficient and relevant answers.

## Features

-   **Offline LLM Inference** using the Ollama 3.1 model
-   **PDF Document Upload & Processing** to extract and index textual content
-   **Context-based Answer Generation** using document chunks for relevant Q&A
-   **Streamlit Interface** for a simple and intuitive user experience

## Prerequisites

-   Python 3.8 or higher
-   Virtual environment management tool (like `venv` or `conda`)
-   Basic understanding of Python and Streamlit

## Installation

### 1. Clone the Repository

`git clone https://github.com/Jatin-Mehra119/local-rag-with-ollama`

`cd local-rag-with-ollama` 

### 2. Set Up a Python Virtual Environment

`python3 -m venv venv` # Create New env

`source venv/bin/activate`   # For Linux/MacOS (Activating env)
# OR
`venv\Scripts\activate`      # For Windows (Activating env)

### 3. Install Dependencies

`pip install -r requirements.txt` 

### 4. Download and Install the Ollama 3.1 Model

Ollama 3.1 LLM is a local large language model used for inference in this app. Follow these steps to download and set up the Ollama model:

1.  **Install Ollama 3.1**: Visit the official [Ollama website](https://ollama.com/) and download the appropriate version for your operating system. Follow the instructions provided for installation.
    
2.  **Download the Llama 3.1 Model**: Once the `ollama` binary is set up, download the model by running:
    `ollama pull llama3.1` 
    

### 5. Run the App

`streamlit run app.py` 

This will launch the app in your default browser at `http://localhost:8501/`.

## Usage

1.  **Upload a PDF Document**: Click on "Upload document" and select a PDF file. The app processes the document and prepares it for answering questions.
2.  **Ask a Question**: Type in a question related to the uploaded document and press Enter. The app retrieves the relevant context from the document and generates an answer.
3.  **Review Responses**: The responses will be displayed in the chat interface.

## Known Issues

-   The model might consume significant memory, depending on the document size and question complexity. For large-scale documents, consider splitting them manually into smaller chunks before uploading.
-   Ensure that the Ollama model is correctly downloaded and available on the local machine for the app to function properly.

## Future Improvements

-   Support for additional document formats (e.g., DOCX, TXT)
-   Enhanced PDF parsing for more accurate context extraction
-   Model fine-tuning capabilities for domain-specific applications

## Contributing

Contributions are welcome! If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are accepted.
