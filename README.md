# RAG_Climate_Change
This project is for implementing a basic Retrieval-Augmented Generation (RAG) system for processing and querying climate related PDF documents. The system encodes the document content into a vector store, which can then be queried to retrieve relevant information.

# Key Components
PDF processing and text extraction
Text chunking for manageable processing
Vector store creation using FAISS and OpenAI embeddings
Retriever setup for querying the processed documents
Evaluation of the RAG system

# Document Preprocessing
The PDF is loaded using PyPDFLoader.
The text is split into chunks using RecursiveCharacterTextSplitter with specified chunk size and overlap.

# Text Cleaning
A custom function replace_t_with_space is applied to clean the text chunks. This likely addresses specific formatting issues in the PDF.

# Vector Store Creation
OpenAI embeddings are used to create vector representations of the text chunks.
A FAISS vector store is created from these embeddings for efficient similarity search.

# Encoding Function
The encode_pdf function encapsulates the entire process of loading, chunking, cleaning, and encoding the PDF into a vector store.

# Retriever Setup
A retriever is configured to fetch the top 2 most relevant chunks for a given query.

# Key Features
Modular Design: The encoding process is encapsulated in a single function for easy reuse.
Configurable Chunking: Allows adjustment of chunk size and overlap.
Efficient Retrieval: Uses FAISS for fast similarity search.
Evaluation: Includes a function to evaluate the RAG system's performance.

# Usage Example
The code includes a test query: "What is the main cause of climate change?". 
This demonstrates how to use the retriever to fetch relevant context from the processed document.

# Evaluation
The system includes an evaluate_rag function to assess the performance of the retriever, though the specific metrics used are not detailed in the provided code.

# Benefits of this Approach
Scalability: Can handle large documents by processing them in chunks.
Flexibility: Easy to adjust parameters like chunk size and number of retrieved results.
Efficiency: Utilizes FAISS for fast similarity search in high-dimensional spaces.
Integration with Advanced NLP: Uses OpenAI embeddings for state-of-the-art text representation.

# Conclusion
This simple RAG system provides a solid foundation for building more complex information retrieval and question-answering systems. By encoding document content into a searchable vector store, it enables efficient retrieval of relevant information in response to queries. 
This approach is particularly useful for applications requiring quick access to specific information within large documents or document collections.
