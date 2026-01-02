# QuickMart | AI-Powered Quick Commerce

![QuickMart Demo](static/images/bananas.png)

QuickMart is a modern Quick Commerce web application that uses **Retrieval-Augmented Generation (RAG)** principles to provide an intelligent product search experience. Instead of simple keyword matching, it understands the *intent* behind a user's query.

## 🚀 Features

*   **AI-Powered Search**: Search for "ingredients for a spicy pasta" and get results like Pasta, Marinara Sauce, and Ground Beef.
*   **Semantic Understanding**: powered by `sentence-transformers` to generate vector embeddings for products.
*   **Minimalist Design**: A clean, "Apple-esque" UI focused on products and usability.
*   **Responsive**: Fully responsive grid layout built with vanilla CSS.
*   **Graceful Degradation**: Falls back to simple keyword search if ML dependencies are missing.

## 🛠️ Tech Stack

*   **Backend**: Python, Flask
*   **AI/ML**: Sentence-Transformers (`all-MiniLM-L6-v2`), Scikit-Learn
*   **Frontend**: HTML5, CSS3 (Variables, Flexbox, Grid), JavaScript (ES6+)
*   **Data**: JSON-based mock database (easily extensible)

## 📦 Installation

1.  **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/quickmart-rag.git
    cd quick_commerce_rag
    ```

2.  **Create a virtual environment**
    ```bash
    python -m venv venv
    # Windows
    venv\Scripts\activate
    # Mac/Linux
    source venv/bin/activate
    ```

3.  **Install dependencies**
    ```bash
    pip install flask sentence-transformers scikit-learn
    ```

4.  **Run the application**
    ```bash
    python app.py
    ```

5.  Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

## 🔮 How it Works

1.  **Ingestion**: On startup, `products.json` is loaded, and text descriptions are converted into vector embeddings using a pre-trained Transformer model.
2.  **Retrieval**: When a user searches, their query is also embedded into a vector.
3.  **Similarity Search**: We calculate the Cosine Similarity between the query vector and all product vectors to find the best semantic matches.
4.  **Response**: The top results are returned to the frontend along with a generated context message.

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
