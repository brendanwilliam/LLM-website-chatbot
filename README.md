# **LLM Website Chatbot**
This toy project lets a user use an LLM to ask questions about a website given a URL. 

*This project is based on [Alejandro AO's tutorial](https://youtu.be/bupx08ZgSFg?si=amzBO15ncv6v96P3).*

## Installation
### 1. Install packages
Run the following command in your terminal. 

*NOTE: If you prefer to set up a virtual environment first, please do so before running this command!*

```
pip install streamlit langchain-core langchain-community langchain-openai
```

### 2. Add OPENAI_API_KEY
Add your personal OpenAI API Key to [`./src/example.env`](.src/example.env) and rename the file to `.env`.

## Run project
Run the following command in your terminal.

```
streamlit run src/app.py
```

## Features and Limiatations
This project takes data from a single URL, adds it to a vector store, and performs a retrieval augmented generation (RAG).

Given a small context window, small vector store, and lack of prompt engineering, this model is prone to hallucinate while filling in gaps of knowledge. Make sure any information you are taking as factual can be verified.
