---
aliases:
  - Retrieval Augmented Generation
  - Retrieval-Augmented Generation
  - RAG
id: 
is:
  - "[[note]]"
is_part_of: "[[ai]]"
---
# Notes
- Retrieval Augmented Generation (RAG) is a technique to improve AI LLM results. It takes an AI prompt, searches a knowledge base for relevant results, then submits the prompt and results to an AI model.
- RAG knowledge bases are typically stored as vector embeddings

## Open Source
https://docs.trychroma.com/
- looks promising
- Can do decent embeddings into it's own vector database, all local
- Issues with latest python version on intel macs, use `pip install onnxruntime==1.16.3` instead
- https://cookbook.chromadb.dev/
- Seems to use cosine distance - https://pub.aimind.so/understanding-cosine-similarity-and-cosine-distance-in-depth-cc91eac3ef2
	- Range from 0 (perfect similarity) to 2 (perfect dissimilarity)