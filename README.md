# Building-RAG-Chatbots-for-Technical-Documentation
A simple RAG chatbot project using LangChain, OpenAI, and Chroma to answer questions from technical car manual documentation.

The chatbot answers user questions based on technical documentation instead of relying only on the model's general knowledge.

## Project Overview

In this project, I used a car warning messages manual as the knowledge source. The document was loaded, split into smaller text chunks, stored in a vector database, and retrieved when the user asked a question.

The final chatbot answered this question:

> "The Gasoline Particular Filter Full warning has appeared. What does this mean and what should I do about it?"

## Final Answer

The Gasoline Particular Filter Full warning indicates that the gasoline particulate filter is full. You should consult an MG Authorised Repairer as soon as possible for assistance.

## Technologies Used

- Python
- LangChain
- OpenAI GPT-4o-mini
- OpenAI Embeddings
- Chroma Vector Database
- Unstructured HTML Loader
- Recursive Character Text Splitter
- Retrieval Augmented Generation

## How the Project Works

1. Load the car manual HTML document.
2. Split the document into smaller text chunks.
3. Convert the chunks into embeddings using OpenAI embeddings.
4. Store the embeddings in a Chroma vector database.
5. Retrieve the most relevant document chunks based on the user query.
6. Send the retrieved context and user question to the language model.
7. Generate a concise answer based only on the manual content.

## Project Structure

```text
RAG_Chatbots/
│
├── data/
│   └── mg-zs-warning-messages.html
│
├── notebook.ipynb
└── README.md
