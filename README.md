📘 Hands-On ML Semantic Search (Word2Vec)

This project is a semantic search system for the book "Hands-On Machine Learning with Scikit-Learn and TensorFlow". It allows users to enter a query and retrieves the top 3 most relevant chunks of text using Word2Vec embeddings combined with TF-IDF weighting.

The interface is built with Gradio for easy interactive use.

🛠 Features

Read a PDF book and split it into manageable chunks.

Preprocess text by removing stopwords, punctuation, and lowercasing.

Generate chunk embeddings using:

Word2Vec model trained on book chunks

TF-IDF weighting to give more importance to unique words

Compute cosine similarity between the query and text chunks.

Retrieve top 3 relevant chunks for any query.

User-friendly Gradio interface for querying the book.

⚡ Installation

Install the required Python packages:

pip install gradio gensim nltk scikit-learn PyPDF2


Note: You may need to download NLTK stopwords and punkt tokenizer:

import nltk
nltk.download('stopwords')
nltk.download('punkt')

📝 Usage

Place your PDF file in the project directory (replace pdf_path with your PDF path in the code).

Run the Python script:

python semantic_search.py


Gradio interface will launch in your browser.

Enter a query in the text box (e.g., "What is machine learning?").

Click Search to get the top 3 most relevant chunks from the book.

🔧 How It Works

Preprocessing: Lowercasing, removing punctuation, tokenization, and stopword removal.

Chunking: Splitting the book text into chunks of ~100 words.

Embeddings:

Train Word2Vec embeddings on chunks.

Compute TF-IDF scores for weighting words.

Combine Word2Vec + TF-IDF to generate chunk embeddings.

Query search:

Preprocess query and compute its embedding.

Compute cosine similarity with all chunk embeddings.

Return top 3 chunks with similarity scores.

🧠 Example

Query: "Neural networks training process"

Output: Top 3 chunks with similarity scores displayed in the interface.

🔗 Dependencies

Python 3.x

Gradio

Gensim

NLTK

Scikit-learn

PyPDF2
