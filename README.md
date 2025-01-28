# Find Similar Images Using Locality Sensitive Hashing (LSH)

This project demonstrates an efficient method for finding similar images using **Locality Sensitive Hashing (LSH)**. The implementation leverages **Apache Spark** for distributed computing, a **pre-trained deep learning model** for feature extraction, and **image embeddings** to identify visually similar images.

## Features

- **Pre-trained Model for Feature Extraction**: Utilizes a deep learning model to generate embeddings for input images, capturing their key visual features.
- **Locality Sensitive Hashing (LSH)**: Efficiently identifies similar embeddings, reducing computational complexity.
- **Apache Spark Integration**: Enables scalable processing of large image datasets across distributed systems.
- **Similarity Search**: Finds images similar to a given query image by comparing their embeddings.

---

## Project Workflow

1. **Environment Setup**:  
   - Import required libraries such as `pyspark`, `tensorflow`, `keras`, etc.
   - Configure Spark for distributed computing.

2. **Feature Extraction**:  
   - Use a pre-trained deep learning model (EfficientNet-B0) to extract feature embeddings from images.
   - Store these embeddings for further processing.

3. **Indexing with LSH**:  
   - Generate hash values for the embeddings using LSH.
   - Create buckets to group similar embeddings.

4. **Query Processing**:  
   - Compute the embedding of a query image.
   - Use LSH to efficiently find embeddings that are similar to the query.

5. **Similarity Scoring**:  
   - Compute similarity metrics (e.g., cosine similarity or Euclidean distance) between the query embedding and retrieved embeddings.
   - Return the most similar images.

---

## Requirements

### Software and Libraries
- **Python 3.8+**
- **Apache Spark** (`pyspark`)
- **TensorFlow** and **Keras** for deep learning
- **Pillow** for image processing
- **Numpy** for numerical computations

## Dataset
- [Flower Images](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/)
## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.
