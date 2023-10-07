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