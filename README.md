# Multi-Stage RAG Failover Agent 

## Objective
This project implements a Multi-Stage Retrieval-Augmented Generation (RAG) pipeline with strict failover logic to handle ambiguous and out-of-domain queries.

The system ensures:
  High precision retrieval
  Query expansion
  Context-only answer generation
  Safe refusal mechanism
  Zero hallucination

---

## System Architecture

User Query  
     ⬇  
R1 – High Threshold Strict Retrieval  
     ⬇  
R2 – Broad Fallback Retrieval  
     ⬇  
R3 – Gemini Query Expansion  
     ⬇  
R4 – Context-Only Synthesis  
     ⬇  
R5 – Final Refusal Logic  

---

##  Requirements Implemented

### R1 – High Threshold Retrieval
  Uses TF-IDF + Cosine Similarity
  Strict similarity threshold (0.8)

###  R2 – Broad Fallback Search
  Lower similarity threshold (0.5)
  Allows moderately relevant matches

###  R3 – Gemini Query Expansion
  Rewrites ambiguous queries
  Improves retrieval quality

###  R4 – Context-Only Synthesis
  Generates answers strictly from retrieved documents
  Prevents hallucination

###  R5 – Final Refusal Logic
  If no relevant context found, system safely refuses

---

##  Technologies Used

  Python
  Scikit-learn (TF-IDF, Cosine Similarity)
  Google Gemini API
  Google Colab
  GitHub

---

##  How to Run

1. Open the notebook in Google Colab
2. Install required libraries
3. Add your Gemini API key
4. Run all cells
5. Test with sample queries

---

## Example Test Queries

  "company profit growth strategy"

---

##  Key Features

  Multi-stage retrieval pipeline
  Threshold-based decision logic
  Failover mechanism
  Safe AI behavior
  No hallucinated answers

---

## 👩‍💻 Author
Mageshwari K
