# Flowise - Corpus-Based Risk Analyzer
## Project Overview
It is a corpus-based risk analyzer built using **Flowise** and **Pinecone (vector store)**.  
It allows users to ask questions about corporate risks and retrieves answers from embedded corporate documents such as HR policies, IT security policies, vendor contracts, and compliance guidelines.

---

## Architecture

![risk-analyzer Architecture](assets/architecture.png)

**Flow:**
1. User submits a query.
2. ChatOpenAI processes the query.
3. Conversational Retrieval Q&A Chain fetches relevant information from:
   - **Pinecone Retriever** (embedded PDFs)
   - **Memory** (conversation history)
4. The system returns answers **only based on retrieved documents**.
5. If no answer is found, it replies: "I don’t know."

---

## Corpus

The system uses embedded PDFs (corporate documents) as the knowledge base. Examples include:

- Corporate HR Policy  
- IT Security Policy  
- Vendor Contract Templates  
- Compliance Guidelines  
- Procurement SOP

> Note: The PDFs are embedded in the vector store and not stored in the repository.

---

## Example Queries

- "Identify compliance risks in the HR policy."  
- "What security risks are mentioned in the IT policy?"  
- "Are there liability clauses in vendor contracts?"  
- "Which operational risks are highlighted in procurement SOP?"  

---

## Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/manissssha1-pixel/flowise-corpus-analyzer.git
cd flowise-corpus-risk-analyzer
