Semantic Search Application using Pinecone
Overview
This project implements a semantic search application using Pinecone, a vector database service. The application allows users to search for similar questions based on input queries.

Features
Utilizes Sentence Transformer for text embedding generation.
Utilizes Pinecone for vector storage and similarity search.
Supports batch processing for efficient indexing.
Provides a query function to find similar questions based on user input.

Includes a basic user interface for demonstration purposes.
Installation
Install the required dependencies:
!pip install pinecone-client
!pip install datasets
!pip install sentence-transformers

Set up your Pinecone API key:
PINECONE_API_KEY = "your_pinecone_api_key"


Run the provided code in a Python environment such as Google Colab or Jupyter Notebook.
Usage

Load the dataset.
Generate embeddings for the questions using Sentence Transformer.
Create an index in Pinecone and upload the embeddings.
Use the provided query function to search for similar questions based on user input.

Run the provided code in a Python environment such as Google Colab or Jupyter Notebook.
Usage
Load the dataset.
Generate embeddings for the questions using Sentence Transformer.
Create an index in Pinecone and upload the embeddings.
Use the provided query function to search for similar questions based on user input.

Example
# Load dataset
dataset = load_dataset('quora', split='train[240000:290000]')

# Generate embeddings
model = SentenceTransformer('all-MiniLM-L6-v2')
query = 'which city is the most populated in the world?'
results = run_query(query)
print(results)
