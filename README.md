# Pharmaceutical Insight Retrieval System

**A Streamlit-based application leveraging advanced Retrieval-Augmented Generation (RAG) techniques to provide insights from pharmaceutical documents.**

---

## **Overview**

The **Pharmaceutical Insight Retrieval System** is designed to help users extract precise and concise information from pharmaceutical research documents. This system utilizes **Google Generative AI Embeddings**, **Chroma** for vector storage, and **Gemini-1.5-pro** LLM to generate answers for user queries, making it an intuitive and powerful tool for real-time document analysis.

---

## **Features**

- **Upload Research Documents**: Users can upload PDFs related to pharmaceutical sciences.
- **Retrieve Relevant Information**: Employs similarity search to fetch the most relevant content from uploaded documents.
- **Dynamic Query Handling**: Generates accurate and concise answers to user queries based on document context.
- **Streamlit UI**: User-friendly interface for interaction.
- **Secure API Integration**: Supports dynamic entry of Gemini API keys via the sidebar.

---

## **Tech Stack**

### **Core Technologies**
- **Streamlit**: For building the interactive user interface.
- **Google Generative AI**:
  - Embedding Model: `models/embedding-001`
  - Language Model: `gemini-1.5-pro`
- **Chroma**: Vector database for storing and retrieving document embeddings.
- **PyPDFLoader**: For loading and parsing PDF documents.
- **SentenceTransformersTokenTextSplitter**: For splitting large texts into manageable chunks with overlapping.

---

## **System Workflow**

1. **Document Upload**:
   - Users upload PDF documents related to pharmaceutical sciences.
   - Documents are processed, split into smaller chunks, and stored in the Chroma vector database with embeddings.

2. **Query Execution**:
   - Users enter a query via the UI.
   - Chroma retrieves the most relevant chunks based on similarity search.
   - Retrieved chunks and the query are passed through a prompt template to the Gemini-1.5-pro model.

3. **Answer Generation**:
   - The Gemini-1.5-pro model generates a concise answer based solely on the retrieved document context.

---

## **How to Run the Project**

### **Prerequisites**
- Python 3.8+
- Install the required libraries using the following command:
  ```bash
  pip install streamlit langchain-google-genai langchain-chroma langchain-community langchain-text-splitters python-dotenv
  ```

### **Steps to Run**

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/pharma-query-system.git
   ```

2. Navigate to the project directory:
   ```bash
   cd pharma-query-system
   ```

3. Create a `.env` file to store your API key:
   ```
   GEMINI_API_KEY=your_api_key
   ```

4. Run the Streamlit application:
   ```bash
   streamlit run app.py
   ```

5. Open the application in your browser at `http://localhost:8501`.

---

## **User Guide**

### **Uploading Documents**
1. Go to the sidebar and upload research documents (PDF format).
2. Click "Submit & Process" to add them to the database.

### **Querying the System**
1. Enter your query in the main input box (e.g., "What are AI applications in drug discovery?").
2. Click "Submit" to get the response.

### **Setting API Key**
- Enter your **Gemini API Key** in the sidebar to enable the system.

---

## **Project Structure**
```plaintext
.
├── app.py               # Main Streamlit application file
├── pharma_db/           # Directory for Chroma vector database
├── temp/                # Temporary directory for uploaded files
├── .env                 # Environment variables (API key)
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation
```

---

## **Future Enhancements**

- Add support for additional file formats (e.g., Word documents).
- Integrate multiple LLMs for comparison.
- Implement advanced analytics for document insights.
- Deploy the application on cloud platforms for broader accessibility.

---

## **Acknowledgments**

This project is built using:
- [Streamlit](https://streamlit.io/)
- [Google Generative AI](https://cloud.google.com/ai)
- [Chroma](https://www.trychroma.com/)
- [LangChain](https://www.langchain.com/)

---

## **Contact**
For queries, reach out to:
- **Pavankumar Kurapati**: [LinkedIn](https://www.linkedin.com/in/pavankumar-kurapati/)

