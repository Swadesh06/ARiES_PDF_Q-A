# ARiES_PDF_Q-A
## What it does ❓
This student project under ARiES club of IITR was aimed at making a working pipeline where in modern AI tools and Language models can be used to perform the task of answering user queries and questions from a pdf

![aries_image](https://github.com/Swadesh06/ARiES_PDF_Q-A/assets/129365476/87a38342-8690-42fd-9981-02c83c9942e8)

# Description 📝

This project demonstrates a streamlined pipeline for answering user queries from PDFs using advanced AI tools and language models, specifically Meta AI’s LLaMA 3 model (8B parameters). Langchain was utilized for creating vector databases from documents, emphasizing efficiency.

The entire project was executed on Google Colab using only free resources. After numerous iterations and experiments, I optimized the methods for compactness and efficiency. The final code is clean and concise after numerous iterations, highlighting the project's practicality and ease of use without relying on APIs or extensive internet access.

## Dataset links 🔗
Alpaca Cleaned Dataset used for Instruction Finetuning - [https://www.kaggle.com/competitions/llm-detect-ai-generated-text/data](https://huggingface.co/datasets/yahma/alpaca-cleaned)


## About the data 📊
-Columns for question (user query) , input for context (data retrieve from vector database while inference) , and response columns to train the adequate response


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



## Brief listing of techniques and tools used for the project: 

- Gathering of larger datasets
- Tokenizinng text for each model
- optmizing model for reduced complexity
- Random Weight Samling to address overfiiting
- Gradiet clipping
- Optimizing tokensation lengths for BERT and RoBERTa by implementing function to decide max_len value
- Tracking progress by progress lines inside the code
- Saving the model weights and tokenized vakues to reduce time taken for subsequent runs in tokensiing
- Saved model first into kaggle working directory and then downloaded and uploaded into input directory to enable offline model running





