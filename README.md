# AI Document Retrieval QA System

## Overview
The AI Document Retrieval QA System is designed to provide personalized information from AI-related documents. The system allows users to upload PDF documents, process and chunk the text, and retrieve answers to questions based on the content of these documents using advanced AI models and vector databases.

## Features
- **PDF Document Processing**: Upload multiple PDF documents and extract text from them.
- **Text Chunking**: Split extracted text into manageable chunks for efficient retrieval.
- **Vector Store**: Utilize Pinecone vector store for storing and retrieving document embeddings.
- **Question Answering**: Ask questions and get relevant answers based on the uploaded documents.
- **Performance Metrics**: Calculate various performance metrics to evaluate the system's effectiveness.

## Getting Started
### Prerequisites
- Python 3.8 or higher
- Required Python packages (listed in `requirements.txt`)

### Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/ai-document-retrieval-qa.git
   cd ai-document-retrieval-qa
2. Create a virtual environment and activate it:
   python -m venv venv
   source venv/bin/activate
3. Install the required packages :
   pip install -r requirements.txt

### Configuration 
Set up API keys for OpenAI and Pinecone in the script:
openai_api_key = "your-openai-api-key"
pinecone_api_key = "your-pinecone-api-key"
pinecone_env = "your-pinecone-environment"


### Running the Application
Run the Streamlit app:

streamlit run AI2.py

Upload PDF documents, enter your question, and get answers based on the content of the uploaded documents.

### Methodology
PDF Text Extraction
Extract text from uploaded PDF files using PyMuPDF.
Chunk the text using RecursiveCharacterTextSplitter to create manageable segments for processing.

Vector Store
Use Pinecone to create and manage a vector store for document embeddings.
Convert text chunks to embeddings using OpenAI's embedding model and store them in the Pinecone index.
Question Answering
Set up a retrieval chain using LangChain to handle context-aware question answering.
Use a system prompt and a question-answer prompt to guide the AI in providing accurate and relevant answers based on document content.

Performance Metrics
Calculate the following metrics to evaluate the system:

Context Precision, Recall, and Relevance
Context Entity Recall
Noise Robustness
Faithfulness
Answer Relevance
Information Integration
Counterfactual Robustness
Negative Rejection
Latency

Proposed Improvements

Enhance the document processing speed and accuracy.
Improve the relevance and precision of retrieved contexts.
Implement better handling of ambiguous or irrelevant questions.
Optimize the performance of the vector store and retrieval chain.

Challenges and Solutions
Challenges

Handling large PDF files and extracting text efficiently.
Ensuring accurate and relevant context retrieval.
Balancing performance and accuracy in question answering.
Solutions

Used PyMuPDF for efficient PDF text extraction.
Implemented a robust text chunking strategy to manage large documents.
Fine-tuned the retrieval chain to improve the accuracy of retrieved contexts.

Future Work

Enhance the system's ability to handle a wider variety of document types and formats.
Integrate additional AI models and techniques for improved answer relevance and accuracy.
Implement more advanced metrics and evaluation techniques to continuously improve the system's performance.

Thankyou!

