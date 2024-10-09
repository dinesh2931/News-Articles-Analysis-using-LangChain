**NewsBot: News Research Tool**
Overview
NewsBot is a Streamlit-based web application designed to analyze and answer questions about news articles. It allows users to input up to three news article URLs and then leverages OpenAI embeddings and FAISS (a fast similarity search library) to create a knowledge base. The user can ask questions, and the app will provide answers, citing sources from the processed articles.

Features
URL Processing: Allows users to input up to 3 URLs of news articles, which the app fetches and processes.
Text Chunking: Splits long articles into manageable chunks for better retrieval accuracy.
Embeddings & FAISS: Uses OpenAI's embeddings model to generate vector representations of text and FAISS for efficient similarity search.
Question Answering: Users can ask questions, and the app retrieves relevant information from the processed articles, providing both answers and cited sources.
Persistence: Saves the FAISS vector store to a pickle file for reuse, so articles do not need to be reprocessed on each run.
How It Works
Input URLs: Users input URLs of news articles they want to analyze.
Process Articles: The application fetches content from the URLs and splits the content into chunks.
Embedding & Vectorization: Using OpenAI embeddings, the content is transformed into a vector format and stored in a FAISS index.
Ask a Question: Users can input queries, and the app will search the vector store to find relevant information, providing answers with sources from the articles.

Steps: 
git clone https://github.com/dinesh2931/News-Articles-Analysis-using-LangChain
pip install requirements.txt
streamlit run app.py
