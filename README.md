

Here is a structured README file for your Streamlit application:  

---

# Chat with PDF Application using Gemini  

This is a **Streamlit**-based application that enables users to upload PDF files, extract their content, and ask questions related to the uploaded files. The application utilizes **Google Generative AI (Gemini)** for embeddings and conversational responses.

---

## Features  
- **PDF Upload**: Users can upload multiple PDF files to the application.  
- **Text Extraction**: Extracts text from the uploaded PDFs using `PyPDF2`.  
- **Text Chunking**: Splits large texts into manageable chunks using `RecursiveCharacterTextSplitter`.  
- **Vector Store Creation**: Builds a vector database using FAISS for efficient similarity search.  
- **Conversational AI**: Leverages Google Gemini (Generative AI) to answer user queries based on the uploaded PDFs.  
- **User Interface**: Simple and interactive UI built with Streamlit.  

---

## Installation  

### Prerequisites  
- Python 3.8 or higher  
- A Google API key with access to Google Generative AI services  
- Required Python libraries:
  - `streamlit`
  - `PyPDF2`
  - `langchain`
  - `langchain_google_genai`
  - `google.generativeai`
  - `faiss-cpu`
  - `python-dotenv`

### Steps  
1. Clone the repository:  
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create and activate a virtual environment:  
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

4. Set up your environment variables:  
   - Create a `.env` file in the root folder.  
   - Add your Google API key:  
     ```plaintext
     GOOGLE_API_KEY=your_google_api_key
     ```

5. Run the application:  
   ```bash
   streamlit run app.py
   ```

---

## Usage  

1. Launch the app by running the above command.  
2. Upload your PDF files through the sidebar uploader.  
3. Once uploaded, the app processes the PDFs to extract text and build the vector database.  
4. Type your questions about the uploaded PDFs in the main input field.  
5. Receive detailed and contextually accurate answers powered by Google Gemini.  

---

## How It Works  

1. **Text Extraction**:  
   The `get_pdf_text` function reads the text from each page of the uploaded PDFs using `PyPDF2`.  

2. **Chunking**:  
   The extracted text is split into smaller chunks using `RecursiveCharacterTextSplitter` to enhance processing efficiency.  

3. **Vector Storage**:  
   Text chunks are embedded using Google Generative AI embeddings and stored in a FAISS vector store for fast similarity search.  

4. **Conversational AI**:  
   User queries are processed by the conversational chain, which retrieves relevant document chunks and generates responses using Google Gemini.

![Flow diagram](https://github.com/user-attachments/assets/e5566803-6261-4d46-bf3d-fcdf6fa8d9ec)

---


## Dependencies  

The following libraries are used in this project:  
- `streamlit`: For building the user interface.  
- `PyPDF2`: For extracting text from PDF files.  
- `langchain`: For managing AI-based workflows.  
- `langchain_google_genai`: For integrating with Google Generative AI.  
- `google.generativeai`: For embeddings and conversational models.  
- `faiss-cpu`: For creating the vector database.  
- `python-dotenv`: For managing environment variables.  

---

## Limitations  

- Requires a Google API key with appropriate permissions.  
- Performance depends on the size of uploaded PDFs and the available resources.  

---

## Future Enhancements  

- Add support for other file types (e.g., Word documents).  
- Enhance the UI for better usability.  
- Implement multi-language support.  
- Add functionality for saving and loading user sessions.  

---

## Author  

Developed with ❤️ by **Vyom Verma**  

Feel free to contribute, report issues, or suggest features!  

---
