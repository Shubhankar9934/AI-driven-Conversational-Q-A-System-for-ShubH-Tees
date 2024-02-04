# AI-Driven-Conversational-SQL-Interaction-System-for-ShubH-Tees-Retail-Shop

## Overview
This project utilizes the LangChain framework to create a system for interacting with a MySQL database using a few-shot learning approach. It incorporates a language model, database utility, and prompts for generating SQL queries based on user questions.

## Setup
1. Install dependencies using `pip install -r requirements.txt`.
2. Create a `.env` file and set your Google API key: `GOOGLE_API_KEY=your_api_key`.

## Components
### 1. Language Model (GooglePalm)
- Utilizes the GooglePalm language model for natural language understanding.

### 2. SQL Database Utility (SQLDatabase)
- Manages connections to a MySQL database using the SQLDatabase utility.

### 3. Vector Store (Chroma)
- Utilizes Chroma to create a vector store for semantic similarity calculations.

### 4. Embeddings (HuggingFaceEmbeddings)
- Incorporates Hugging Face embeddings for transforming text data.

### 5. Few-Shot Learning
- Implements a few-shot learning approach for generating SQL queries.

## Configuration
- Configure database parameters (user, password, host, name) in the script.
- Set the Hugging Face model name for embeddings.
- Define a few-shot prompt template for generating examples.

## Usage
1. Run the script to initialize the LangChain SQLDatabaseChain.
2. Interact with the system using user queries and receive SQL query suggestions.

## Example
```python
from your_script import get_few_shot_db_chain

# Initialize the LangChain SQLDatabaseChain
chain = get_few_shot_db_chain()

# Use the chain to interact with the MySQL database
result = chain.process_user_input("How many products were sold today?")
print(result)
