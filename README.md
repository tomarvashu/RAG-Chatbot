# RAG Chatbot

A Retrieval-Augmented Generation chatbot workflow built in n8n using MongoDB Atlas Vector Search and OpenAI. The system ingests documents from Google Drive into a vector store, then uses an AI agent with memory and retrieval to answer user questions with knowledge-backed responses.

## My Role
I initiated this project, defined the retrieval workflow and interaction logic, and actively contributed to its design and refinement. Development was carried out with support from my internal team, while I remained involved in testing, iteration, and execution review.

## What It Does
- Watches a document in Google Drive
- Downloads the file automatically
- Loads document content into a vector store
- Creates embeddings using OpenAI
- Stores vectors in MongoDB Atlas
- Exposes a chat-triggered AI agent
- Uses retrieval as a tool for knowledge-based answers
- Maintains short chat memory in MongoDB

## Workflow Overview
### Document Ingestion
1. Google Drive Trigger watches a specific file
2. The file is downloaded automatically
3. The document is loaded through a default data loader
4. OpenAI embeddings are created
5. The content is inserted into MongoDB Atlas Vector Store

### Chat / Retrieval
1. A chat trigger receives the user message
2. The AI Agent processes the request
3. OpenAI Chat Model powers the response
4. MongoDB Chat Memory keeps recent conversation context
5. MongoDB Atlas Vector Store is used as a retrieval tool
6. The agent answers using the ingested knowledge base

## Tech Stack
- n8n
- OpenAI
- MongoDB Atlas Vector Search
- MongoDB Chat Memory
- Google Drive
- RAG workflow
- JavaScript / workflow logic

## Use Case
This workflow is useful for building internal knowledge assistants, document Q&A systems, and AI chat interfaces that need grounded responses from uploaded files.

## Notes
Before publishing publicly, remove or replace:
- private file IDs
- private database names
- private collection names
- internal credentials
- company-specific documents
