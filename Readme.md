# RAG Systems Learning Journey

## Project Overview
This project demonstrates the implementation and evaluation of different RAG (Retrieval Augmented Generation) approaches using LlamaIndex and TruLens. The project focused on building and comparing various query engines to effectively retrieve and process information from a PDF document about AI careers.

## Key Learning Points

### 1. Document Processing
- Learned to load and process PDF documents using SimpleDirectoryReader
- Understood document chunking and indexing strategies

python
from llama_index import SimpleDirectoryReader
documents = SimpleDirectoryReader(input_files=["./eBook-How-to-Build-a-Career-in-AI.pdf"]).load_data()

### 2. RAG Implementation Approaches
- **Basic Vector Store Index**: Implemented simple vector-based retrieval
- **Sentence Window Retrieval**: Created more context-aware retrievals using sentence windows
- **Auto-merging Retrieval**: Learned advanced document chunking and merging strategies

### 3. Query Engine Types
- Built and compared different query engines:
  - Basic Query Engine
  - Sentence Window Query Engine
  - Auto-merging Query Engine
- Understood the strengths and use cases for each approach

### 4. Evaluation Framework
- Implemented evaluation using TruLens
- Created feedback functions for measuring:
  - Answer relevance
  - Context relevance
  - Response faithfulness
- Learned to compare performance across different RAG approaches

### 5. Advanced Features
- Document chunking strategies
- Node parsing and merging
- Response synthesis
- Context window optimization

## Technologies Used
- LlamaIndex
- TruLens
- OpenAI API
- Python
- Jupyter Notebooks

## Key Components

### Vector Store Setup
python
from llama_index import VectorStoreIndex
index = VectorStoreIndex.from_documents([document], service_context=service_context)

### Sentence Window Implementation
python
from llama_index.node_parser import SentenceWindowNodeParser
sentence_window_engine = get_sentence_window_query_engine(sentence_index)

## Results and Observations
- Sentence window retrieval provided more contextual responses
- Auto-merging approach showed better handling of complex queries
- Evaluation metrics helped quantify the performance differences between approaches

## Future Improvements
- Implement more sophisticated evaluation metrics
- Experiment with different embedding models
- Optimize chunk sizes for better retrieval
- Explore hybrid retrieval approaches

## Getting Started
1. Install required dependencies
2. Set up OpenAI API key
3. Prepare your document dataset
4. Run the notebooks in sequence:
   - L1-Advanced_RAG_Pipeline
   - L2-RAG_Triad_of_metrics
   - L3-Sentence_window_retrieval
   - L4-Auto-merging_Retrieval

## Resources
- LlamaIndex Documentation
- TruLens Documentation
- OpenAI API Documentation