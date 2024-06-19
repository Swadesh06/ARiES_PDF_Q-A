# ARiES_PDF_Q-A
This student project under ARiES club of IITR was aimed at making a working pipeline where in modern AI tools and Language models can be used to perform the task of answering user queries and questions from a pdf

![aries_image](https://github.com/Swadesh06/ARiES_PDF_Q-A/assets/129365476/87a38342-8690-42fd-9981-02c83c9942e8)



## Dataset links:
Alpaca Cleaned Dataset used for Instruction Finetuning - [https://www.kaggle.com/competitions/llm-detect-ai-generated-text/data](https://huggingface.co/datasets/yahma/alpaca-cleaned)


## About the data
### Given Datset-
-Columns for question (user query) , input for context (data retrieve from vector database while inference) , and response columns to train the adequate response



## Setup:

- setup for each model used is given separately below:

  ### DistilBERT(public score 0.803) :
  
<img width="294" alt="Screenshot 2024-01-15 at 10 00 56 PM" src="https://github.com/Swadesh06/LLM-AI-Genrated-Text-Classification/assets/129365476/17bc2e7f-6a64-48fd-9220-3383c62e517b">

In this setup I also downloaded the output files after the first Internet "on" run and uploaded them into the input directory so as to save the effort of having to have a first run with intenet on whenever I opened the notebpok again.


 ### RoBERTa (public score 0.672 ):
 
<img width="392" alt="Screenshot 2024-01-15 at 10 10 20 PM" src="https://github.com/Swadesh06/LLM-AI-Genrated-Text-Classification/assets/129365476/be025669-4a2c-48a2-bf24-ed7c42a69f80">

RoBERTa performed poorer despite being a more adavnced model due to overfitting and lack of optimization to make the suitable tokenizing changes. I implemented them later but some changes were left to be accomodated and time didn't allow for them.

### BERT (public score N/A) :

<img width="408" alt="Screenshot 2024-01-15 at 10 04 34 PM" src="https://github.com/Swadesh06/LLM-AI-Genrated-Text-Classification/assets/129365476/5576d19f-0469-4718-bbe4-329841930082">

BERT took a very long time to train and I was unsucessful in getting a complete first run on the dataset , so I couldn't save the model in time for submission, and had to leave the tokenzier files in the output directory itself.

I did manage to save the tokenized values but they were later deemed unnecessary due to the firther optimisations I made in the tokenisation process of BERT

## Steps Taken:

- Gathering of larger datasets
- Tokenizinng text for each model
- optmizing model for reduced complexity
- Random Weight Samling to address overfiiting
- Gradiet clipping
- Optimizing tokensation lengths for BERT and RoBERTa by implementing function to decide max_len value
- Tracking progress by progress lines inside the code
- Saving the model weights and tokenized vakues to reduce time taken for subsequent runs in tokensiing
- Saved model first into kaggle working directory and then downloaded and uploaded into input directory to enable offline model running





