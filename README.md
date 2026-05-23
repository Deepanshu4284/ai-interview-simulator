# AI Interview Simulator

A local-only, full-stack AI interview simulator that analyzes candidate resumes, extracts skills, and generates context-aware interview questions using a local LLM.

## Features
- **Local AI Processing**: Uses a local Ollama LLM for generating questions and evaluating answers, ensuring privacy and offline capability.
- **Resume Parsing & Skill Extraction**: Automatically parses uploaded resumes (PDF/DOCX) and extracts key skills.
- **RAG-based Context Retrieval**: Utilizes FAISS and MiniLM for context retrieval, ensuring interview questions are highly relevant to the candidate's specific background.
- **Performance Tracking**: Stores user accounts, sessions, and interview performance metrics using a local SQLite database.
- **Responsive Frontend**: Clean, user-friendly interface built with modern web technologies.

## Tech Stack
- **Backend**: FastAPI (Python), SQLite
- **AI/ML**: Ollama (LLM), FAISS (Vector DB), SentenceTransformers (MiniLM)
- **Frontend**: HTML, CSS, JavaScript

## Setup Instructions

### Prerequisites
- Python 3.8+
- [Ollama](https://ollama.ai/) installed and running locally with the required model (e.g., `llama3` or `mistral`).

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Create and activate a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the backend server:
   ```bash
   uvicorn main:app --reload
   ```
   The backend will be available at `http://localhost:8000`.

### Frontend Setup
1. Simply open the `frontend/index.html` file in your preferred web browser, or serve it using a local HTTP server:
   ```bash
   cd frontend
   python3 -m http.server 3000
   ```
2. Access the frontend at `http://localhost:3000`.

## Usage
1. Create an account and log in.
2. Upload your resume to begin a new interview session.
3. Answer the AI-generated questions based on your resume context.
4. Receive a final score and feedback on your performance.

## License
MIT License
