# 🌐 News Research Tool for Equity Analysis

## Overview

The **News Research Tool for Equity Analysis** is an innovative chatbot 🤖 designed to assist equities research analysts in efficiently extracting and summarizing financial data 📊 from a variety of news articles. By utilizing cutting-edge technologies like **Streamlit**, **Langchain**, and **ChatGroq**, this tool automates data extraction and query handling, enhancing the accuracy and speed of information retrieval.

## Key Features

- 📰 **Automated data extraction** from news articles
- 🖥️ **User-friendly interface** built with Streamlit
- ✅ **Retrieval-based quality assurance** using vector databases
- 📝 **Summarization of financial data** to support investment decisions
- 📈 **Scalable architecture** suitable for large datasets


## Introduction

In today's world 🌍, where AI is revolutionizing how we manage tasks, this tool aims to enhance the way analysts conduct equity research. The chatbot provides answers and summaries based on user input and can be used to analyze various financial news articles. It helps streamline the research process for better investment decision-making 💡.


### Why Build This Chatbot?

1. **Tedious Copy-Pasting**: Research analysts often have to read multiple articles to gather information. This can involve a lot of copying and pasting text from different sources, which is not only time-consuming but also boring. Since they are busy professionals, they need a more efficient way to collect information without spending hours on repetitive tasks.

2. **Need for an Aggregate Knowledge Base**: When research analysts ask questions, they might not know where the best answers will come from. They often pull information from various websites, but it can be hard to tell if those sources are reliable or relevant. A chatbot can help by collecting and organizing information in one place, making it easier for analysts to find accurate answers quickly.

3. **Limitations of ChatGPT**: While ChatGPT is a powerful tool, it has limitations, such as a word count restriction. This means that analysts might not be able to get all the information they need in one go. The chatbot we’re building can help overcome this by providing more comprehensive answers without the same constraints, allowing analysts to get the detailed information they require for their research. 

### Summary
In short, this chatbot aims to make the research process for equity analysts faster and easier by reducing tedious tasks, organizing knowledge, and providing thorough answers without limitations.


## Proposed System

### Functional Description

The proposed system is a news research tool that simplifies the retrieval and summarization of content for equity research analysts. Users can enter URLs of articles and ask questions related to the Equity. The system responds with relevant information🔍.

### Proposed Solution Architecture

- **User Interface (UI)**: Built with Streamlit to allow user queries and URL input and Displaying results.

#### Backend Processing

- **Text Loader**: We had imported textloader library which allows to import data from text file.
- **Unstrctured URL Loader Class**: It uses the Library called Unstructured and basically go to that website; look into the dom object or the HTML Strcture of the page, and pulls all the information.
- **Text Splitting**: Using `CharacterTextSplitter` and `RecursiveCharacterTextSplitter` classes because LLM is having token size limit. Soo these classes helps in reducing big block of text into smaller chunks for faster processing.
- **Embedding Creation**: Converting chunks into embeddings using OLLAMA Model.
- **Using FAISS Vector Database**: Utilizes **FAISS** to store relevant vectors and can do Similarity Search.
- **Question Answering**: Implements a QA retrieval chain to process user inquiries against the embedded documents.

## Software Requirements

- **Programming Languages**: Python 🐍
- **Libraries and Frameworks**:
  - **Streamlit** (for building UI)
  - **unstructured** (for URL loaders)
  - **FAISS** (for vector database)
  - **Ollama** (for creating embeddings)
  - **Chatgroq** (for API integration)
  - **Pickle** (for serialization)
  - Other dependencies: **numpy**, **pandas**, etc.

## Hardware Requirements

- **Development Environment**:
  - Modern personal computer 💻 with at least **8 GB RAM** and a **4-core CPU**.
  - **Internet connection** for API access and data retrieval 🌐.

## Deployment Environment

- Server with sufficient **CPU**, **RAM**, and **storage** based on expected usage.
- **GPU** may be advantageous for faster processing with large datasets and complex embeddings ⚡.
