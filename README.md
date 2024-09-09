# LangChain-PDF-QA

LangChain-PDF-QA is a Python-based project that uses the LangChain framework to generate questions and answers from PDF documents. It’s designed to help programmers and students prepare for coding exams by creating practice questions based on the content of coding materials.

## Features

- **PDF Processing**: Extracts text from PDF files.
- **Question Generation**: Generates relevant questions from the extracted text to help in exam preparation.
- **Answer Generation**: Uses embeddings and vector stores to provide answers to the generated questions.
- **Output to CSV**: Saves the generated questions and answers into a CSV file.

## Installation

To get started, clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/yourusername/LangChain-PDF-QA.git
```
## Usage

Alternatively, you can directly install the required packages using the following command:

```bash
pip install langchain langchain_community PyPDF2 pypdf ctransformers sentence_transformers faiss-gpu
```
## Usage Steps

1. **Place your PDF file** in the project directory.

2. **Modify the `file_path` variable** in the script to point to your PDF file.

3. **Run the script to generate questions and answers:**

    ```bash
    python main.py
    ```

   The generated questions and answers will be saved in `QA.csv`.

## How It Works

1. **Load PDF**: The `PyPDFLoader` extracts content from the provided PDF file.

2. **Text Splitting**: The content is split into manageable chunks using `RecursiveCharacterTextSplitter`.

3. **Question Generation**: The extracted text is passed through a Language Model to generate practice questions.

4. **Answer Retrieval**: A FAISS vector store is used to retrieve and generate answers from the extracted content.

5. **Save to CSV**: The generated questions and answers are saved in a CSV file for easy access.

## Example

```python
file_path = "./PDF_PATH.pdf"  # Replace with your PDF file path
generate_questions_and_answers(file_path)
```
## Dependencies

- **LangChain**: A framework for developing applications powered by language models.
- **LangChain Community**: Community-driven extensions and tools for LangChain.
- **PyPDF2**: A library for reading and manipulating PDF files in Python.
- **PyPDF**: A library for splitting, merging, and working with PDF files.
- **ctransformers**: A library for using Transformer models.
- **Sentence Transformers**: A library for sentence embeddings using Transformer models.
- **FAISS-GPU**: A library for efficient similarity search and clustering of dense vectors, optimized for GPU usage.

