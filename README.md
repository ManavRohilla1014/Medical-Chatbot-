## About The Project

This project leverages natural language processing and information retrieval techniques to create an interactive system for answering user queries based on a collection of PDF documents. The process begins with loading and segmenting PDFs into smaller text chunks. These chunks are then embedded using a pre-trained Hugging Face model. The embeddings are indexed using Pinecone, a vector search engine, facilitating efficient similarity searches. User queries are processed using a retrieval question-answering (QA) system, which combines the Pinecone index, a language model loaded from a file, and a defined prompt template. The project aims to provide concise and accurate responses to user queries, fostering a seamless interaction between the user and the information stored in the PDF documents.


# How to run?
### STEPS:

Clone the repository

```bash
Project repo: https://github.com/
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.10 -y
```

```bash
conda activate medibot
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


### Create a `.env` file in the root directory and add your Pinecone & openai credentials as follows:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
OPENAI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


```bash
# run the following command to store embeddings to pinecone
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost:
```


### Techstack Used:

- Python
- LangChain
- Flask
- GPT
- Pinecone
