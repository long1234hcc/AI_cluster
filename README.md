# Product Name Clustering using FAISS & BGE-M3 Embeddings
## Project Purpose: Develop a vector-based product clustering system for e-commerce data using FAISS, BGEM3FlagModel, and cosine similarity. The system groups similar product names based on embeddings to improve search, categorization, and product recommendations.

## Project Description
1. Data Preprocessing:
  + Read product data from an Excel file.
  + Normalize text and remove brand names from product names.
    
2. Embedding Generation:
  + Use BGEM3FlagModel (BAAI/bge-m3) to generate vector embeddings for product names.
  + Process embeddings in batches to optimize performance.
    
3. Vector Database Construction:
  + Store embeddings in a FAISS index for efficient similarity search.
  + Use cosine similarity as the distance metric.
  + Deploy FAISS on GPU for faster computation.
    
4. Product Clustering:
  + Perform nearest neighbor search in FAISS.
  + Group similar products based on a cosine similarity threshold (default: 0.85).
  + Assign a unique group label to each product.

5. Encoding Group Labels:
  + Convert product group labels into numerical IDs using LabelEncoder for further analysis.

## Project Operation Steps
1. Load and preprocess product data (normalize names, remove brand names).
2. Generate BGE-M3 embeddings for all products.
3. Build a FAISS index and normalize embeddings.
4. Perform nearest neighbor search to find similar products.
5. Assign group labels based on similarity threshold.
6. Convert group labels into numerical encodings for analysis.
