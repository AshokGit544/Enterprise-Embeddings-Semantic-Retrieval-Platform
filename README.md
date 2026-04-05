# Enterprise Embedding-Oriented Semantic Retrieval Platform for Engineering, Quality, and Manufacturing Documents

## Project Overview
This project simulates how embeddings can be used to improve semantic retrieval across complex enterprise documents.

It is based on a document retrieval pattern where keyword search alone is not enough, so documents are prepared as vector-friendly chunks with metadata enrichment to support semantic retrieval across engineering, quality, and manufacturing use cases.

The project includes:
- synthetic enterprise document generation
- metadata extraction and enrichment
- vector-friendly chunk creation
- simple embedding generation using TF-IDF vectors
- semantic similarity search demo
- search-ready output records

## Business Goal
The goal of this project is to show how embedding-oriented pipelines improve semantic retrieval and make enterprise search more useful for engineering, quality, and manufacturing document use cases.

## Tools Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Google Colab


### Sample Semantic Search Output

For the query:

`engineering document about sensor failure on equipment EQP1002 in plant PLT200`

the retrieval pipeline returned the following top matching document chunks ranked by similarity score.

| Rank | Chunk ID         | Document ID | Domain        | Document Type       | Plant   | Supplier | Equipment | Date       | Similarity Score |
|------|------------------|-------------|---------------|---------------------|---------|----------|-----------|------------|------------------|
| 1    | DOC00220_CHUNK_1 | DOC00220    | engineering   | engineering_change  | PLT200  | Aptiv    | EQP1002   | 2024-09-07 | 0.553501         |
| 2    | DOC00011_CHUNK_1 | DOC00011    | engineering   | engineering_change  | PLT200  | Denso    | EQP1002   | 2024-11-03 | 0.545139         |
| 3    | DOC00289_CHUNK_1 | DOC00289    | engineering   | supplier_record     | PLT200  | Aptiv    | EQP1002   | 2024-12-21 | 0.522913         |
| 4    | DOC00053_CHUNK_1 | DOC00053    | quality       | engineering_change  | PLT200  | Denso    | EQP1002   | 2024-11-05 | 0.514800         |
| 5    | DOC00244_CHUNK_1 | DOC00244    | engineering   | engineering_change  | PLT200  | Lear     | EQP1002   | 2024-02-25 | 0.513283         |

**Observation:**  
The highest-ranked results matched the main business conditions from the query, especially:
- domain = engineering
- plant = PLT200
- equipment = EQP1002

This shows that the retrieval pipeline is correctly identifying the most relevant document chunks using metadata-aware semantic search.

## Final Pipeline Summary

The pipeline execution summary provides a quick overview of the overall processing and results.

### Summary Details

- **Total Documents Processed:** 300  
- **Total Chunks Created:** ~600+  
- **Vector Records Generated:** ~600+  
- **Query Used:**  
  `engineering document about sensor failure on equipment EQP1002 in plant PLT200`  

- **Top Matching Document:**  
  DOC00220  

### What this means
The system successfully processed enterprise documents, converted them into searchable format, and returned the most relevant document based on the given query.
