# Topic Modeling with Llama 2 (using BERTopic)
This project explores topic modeling using Llama 2 without requiring every document to be passed directly to the model. Instead, BERTopic, a modular topic modeling technique, is leveraged to fine-tune topic representations using LLMs (Large Language Models).

## Key Steps in BERTopic
- Embedding Documents - Converting text into numerical vectors.
- Dimensionality Reduction - Reducing embedding size for efficient processing.
- Clustering - Grouping similar texts into topics.
- Tokenizing Documents - Splitting text into meaningful components.
- Extracting Representative Words - Identifying key terms for each topic.

## Why Use Llama 2?
- Instead of simple word lists, Llama 2 helps refine topic labels, making them more interpretable.
- Directly passing all documents to Llama 2 would be computationally expensive, so vector databases and BERTopic representations are used instead.

## Implementation Details
- Data Source: ArXiv abstracts (diverse, structured, topic-rich).
- Model Used: meta-llama/Llama-2-13b-chat-hf, optimized using 4-bit quantization for efficient execution on a T4 GPU.
- Prompt Engineering: Custom templates guide Llama 2 to generate structured topic labels.
- Embedding Model: BAAI/bge-small-en for converting abstracts into vectors.
- Dimensionality Reduction & Clustering: Using UMAP for dimensionality reduction and HDBSCAN for topic clustering.
- Topic Representations: Multiple representations, including c-TF-IDF, KeyBERT, Maximal Marginal Relevance (MMR), and Llama 2 for enhanced labeling.

## Results & Visualization
- **100+ topics generated** with diverse themes.
- **Llama 2-generated topic labels** improve interpretability over traditional methods.
- **Interactive visualization** using BERTopic’s visualize_documents() function to explore topic distributions.

## Conclusion
This project demonstrates an efficient and scalable approach to topic modeling with Llama 2 and BERTopic. It leverages advanced NLP techniques to generate interpretable, high-quality topic representations, making it a valuable tool for organizing and analyzing large text datasets.







