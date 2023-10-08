## Vector Databases

Task:  Follow Official QDrant Tutorial

* Semantic Search [Tutorial from qdrant](https://github.com/qdrant/landing_page/blob/master/qdrant-landing/content/documentation/tutorials/search-beginners.md)

Task:  Run Qdrant Rust Client

* Checkout repo:  https://github.com/qdrant/rust-client
* Run DB:  
```bash
docker run -p 6333:6333 -p 6334:6334 \
    -e QDRANT__SERVICE__GRPC_PORT="6334" \
    qdrant/qdrant
```
* `cargo run --example search`


![Screenshot 2023-10-08 at 10 21 09 AM](https://github.com/nogibjj/vector-graph-db/assets/58792/e94818a2-b915-4ebe-be5f-9a1eec96c8d6)


### Lab Task:  Extend Semantic Search

#### Learning Objectives
By the end of this lab, you will be able to:

* Launch a GitHub Codespace with the lab environment set up
* Install Qdrant and SentenceTransformers packages
* Load sample book metadata
* Create a Qdrant collection and index book vectors
* Query the collection semantically based on book descriptions
* Filter results by publication year

#### Instructions

1. Launch GitHub Codespace
Follow the link provided to launch the lab codespace on GitHub.
Once it builds, you will have a containerized development environment ready.
2. Install Packages
Run the provided setup script to install Qdrant and SentenceTransformers.
3. Load Book Data
Import the sample book metadata provided in books.py.
4. Create Qdrant Collection
Initialize a Qdrant client pointed to in-memory storage.
Create a collection for the book vectors.
5. Index Book Vectors
Use SentenceTransformers to encode each book description into a vector.
Upload the encoded vectors along with metadata to Qdrant.
6. Execute Search Query
Encode a sample query string into a vector.
Use this vector to query the collection and return similar books.
7. Add Year Filter
Modify the query to only return recent books from the 2000s.

### Challenge Activities

These optional challenges allow you to explore Qdrant further:

* Load a larger dataset like Wikipedia summaries
* Benchmark search performance for different vector sizes
* Add multiple filters on metadata like author name
* Visualize vectors in 2D/3D using PCA
