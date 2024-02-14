# LLM-Powered Chatbot with Retrieval Augmented Generation

This repository hosts a chatbot powered by OpenAI's language models (LLM) and incorporates functionality for extracting text from PDF files, embedding the information and creating a retrieval mechanism to answer user's queries based on the provided data. This is incredibly beneficial when we need the chatbot to answer use case specific queries or about the information that the LLM was not been trained on. The project consists of two main methods defined under two main scripts:

## File 1: Chatbot with OpenAI Models (data is stored on a github folder) with RAG Capability
- **Script:** `rag_with_default_file.py`
- **Description:**
  - Utilizes Streamlit for a user-friendly chat interface.
  - Uses llama_index to read the data from a pdf and index it.
  - Implements OpenAI's GPT-3.5-turbo model to answer queries related to the files present in the data folder.(in this case: Regulations in PART 86—CONTROL OF EMISSIONS FROM NEW AND IN-USE HIGHWAY VEHICLES AND ENGINES within the Code of Federal Regulations.)
  - Provides citations and elucidates concepts by referencing relevant sections and sub-sections.

### Usage
1. Run the script using `python rag_with_default_file.py`.
2. Input queries regarding emission control regulations in the specified document.

## File 2: Chatbot with OpenAI Models (data is uploaded by the user) with RAG Capability
- **Script:** 'rag_with_file_input.py`
- **Description:**
  - Uses Streamlit to create a chat-like interface for user interaction.
  - Employs Langchain library for PDF text extraction and vectorization using OpenAI embeddings.
  - Enables users to upload PDF files, processes them, and uses OpenAI's GPT-3.5-turbo model to answer queries.

### Usage
1. Run the script using `python rag_with_file_input.py`.
2. Upload PDF files and click the "Process" button to extract text and set up a conversation chain.
3. Ask questions related to the content of the uploaded PDF.

## Dependencies
Ensure you have the necessary dependencies installed by running:
```bash
pip install -r requirements.txt
```

## Configuration
- For the OpenAI API key, create a `secrets.toml` file and store the key as `openai_key` for `llm_chatbot.py` and as `openai_api` for `pdf_text_extraction.py`.

## Contributing
Feel free to contribute to the project by opening issues or submitting pull requests. Your feedback and contributions are highly appreciated.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
