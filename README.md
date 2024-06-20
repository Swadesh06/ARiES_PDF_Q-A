# ARiES_PDF_Q-A
## What it does ❓
This student project under ARiES club of IITR was aimed at making a working pipeline where in modern AI tools and Language models can be used to perform the task of answering user queries and questions from a pdf

![aries_image](https://github.com/Swadesh06/ARiES_PDF_Q-A/assets/129365476/87a38342-8690-42fd-9981-02c83c9942e8)

## Description 📝

This project demonstrates a streamlined pipeline for answering user queries from PDFs using advanced AI tools and language models, specifically Meta AI’s LLaMA 3 model (8B parameters). Langchain was utilized for creating vector databases from documents, emphasizing efficiency.

The entire project was executed on Google Colab using only free resources. After numerous iterations and experiments, I optimized the methods for compactness and efficiency. The final code is clean and concise after numerous iterations, highlighting the project's practicality and ease of use without relying on APIs or extensive internet access.

## Dataset links 🔗
Alpaca Cleaned Dataset used for Instruction Finetuning - [[https://www.kaggle.com/competitions/llm-detect-ai-generated-text/data](https://huggingface.co/datasets/yahma/alpaca-cleaned)](https://huggingface.co/datasets/yahma/alpaca-cleaned)


## About the data 📊
Columns for question (user query) , input for context (data retrieve from vector database while inference) , and response columns to train the adequate response


## Installations 🔧

Dependencies:

- Python==3.10.12
- langchain==0.0.190
- langchain-community==0.0.3
- pypdf==3.8.1
- fitz==0.0.1.dev2
- pymupdf==1.19.6
- unstructured==0.6.4
- python-magic==0.4.27
- faiss-gpu==1.7.3
- transformers==4.27.4
- torch==2.0.1
- huggingface_hub==0.14.1
- python-dotenv==1.0.0
- streamlit==1.22.0
- tiktoken==0.4.0
- protobuf==3.20.3
- sentence-transformers==2.2.2
- xformers==0.0.16
- trl==0.8.0
- peft==0.3.0
- accelerate==0.20.3
- unsloth[colab-new] @ git+https://github.com/unslothai/unsloth.git
- bitsandbytes==0.38.1

## Setup ⚙️

<img width="709" alt="Screenshot 2024-06-20 at 1 04 01 PM" src="https://github.com/Swadesh06/ARiES_PDF_Q-A/assets/129365476/b60247b8-c0fe-4380-a9d5-800b40dfaabe">



## Brief listing of techniques and tools used for the project 💡

- Dataset used for training : Alpaca cleaned
- Unsloth library used for faster fine-tuning and also memory management
  - Optimisations within the library to improve speed and effecency are:
    
    1. Manual Autograd ensures that the backpropagation process is highly optimized for the specific architecture,               reducing training time.
    2. Chained Matrix Multiplication speeds up the key matrix operations in the transformer layers, improving throughput.
    3. Triton Language Kernels optimize the low-level operations on the GPU, making the most of the available hardware           resources.
    4. Flash Attention makes the attention mechanism more efficient, allowing the model to process larger inputs and             focus on important data, enhancing both speed and accuracy.

- Recursive Character Cplitting for splitting exttacted text form the document into smaller chunks of data
- Optimizing max_length for context window for LLaMA3 - 8B to increase context size from 8192, using RoPE scaling, which after much slow implemeentations was found implemnted in the Unsloth Library. Context length can theoretically be taken to any size , but make sure to then train it on data suiting the context window otherwise the answers seem to turn nonsensical for very high context window lengths
- Sentence Transformers (all-MiniLM-L6-v2) used for text embeddings (384 dimensional) of the chunks.
- FAISS (FAcebook AI Similarity Search) vector database used for creating a database with the embedded chunk vectors of   the document(s).
- Similarity search retrieval (with score) is used to retrieve relevant documents to the user query
- Retrieval Augmented Generation (RAG) used for compiling the user query and assigning question, inout data for context, and response roles
- Saving the LoRA adapter of the model to later download it faster and with computational ease
- Save the document database so that you don't have to create the database once again for the same document(s).

## Documentation 📑
- HLD : https://docs.google.com/document/d/1TSAjd81z32yjWSlfPjMyWigkMKMOzUjUYDxBR5RmJyI/edit?usp=sharing



