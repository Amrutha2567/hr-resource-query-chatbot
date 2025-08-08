# HR Resource Query Chatbot

## Overview
A FastAPI-based chatbot that helps HR teams find suitable employees for tech projects using natural language queries.

## Features
- Employee data search via API
- Natural language query processing
- Basic keyword-based retrieval
- 15 sample employee profiles

## Architecture
- FastAPI for backend
- JSON for data layer
- Simple retrieval-augmentation-generation flow (non-LLM)

## Setup & Installation
```bash
pip install -r requirements.txt
uvicorn main:app --reload
```
Access at: http://127.0.0.1:8000/docs

## API Documentation
- `POST /chat` – Input a natural language query
- `GET /employees/search?skill=Python&min_experience=3`

## AI Development Process
- Used ChatGPT for architecture, code suggestions, and sample data generation.
- 70% AI-assisted (data + endpoint generation), 30% manual (wiring + testing)
- AI couldn't handle custom filtering logic perfectly – manually resolved

## Technical Decisions
- FastAPI for speed and auto docs
- Simple Python embedding for retrieval (no LLM used yet)
- Chose non-LLM due to time/cost

## Future Improvements
- Integrate OpenAI or Ollama for full RAG
- Vector database (e.g., FAISS)
- Streamlit frontend

## Demo
Run locally with: `uvicorn main:app --reload`
