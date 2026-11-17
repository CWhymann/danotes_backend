# DaNotes Backend API

This repository contains the backend API for the DaNotes application. It is built using Django and Django REST Framework (DRF) and provides endpoints to manage notes.

## Tech Stack

- **Framework:** Django
- **API:** Django REST Framework
- **Database:** SQLite (Development environment)

## Local Setup

1. Clone the repository:
   git clone https://github.com/CWhymann/danotes_backend.git
   cd danotes_backend

2. Create and activate a virtual environment:
   python -m venv .venv
   # Windows:
   .venv\Scripts\activate
   # macOS/Linux:
   source .venv/bin/activate

3. Install dependencies:
   pip install -r requirements.txt

4. Apply migrations:
   python manage.py migrate

5. Start the server:
   python manage.py runserver

## API Reference

The API is accessible at `http://127.0.0.1:8000/api/`.

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| GET | `/api/notes/` | Retrieves a list of all notes. |
| POST | `/api/notes/` | Creates a new note. |
| GET | `/api/notes/{id}/` | Retrieves a specific note. |
| PUT | `/api/notes/{id}/` | Updates a specific note. |
| DELETE | `/api/notes/{id}/` | Deletes a specific note. |

### Data Model
The `Note` model contains: `id`, `title`, `content`, `marked` (boolean), and `trash` (boolean).

## Integration
CORS is configured to allow requests from the Angular frontend. The expected endpoint for the frontend is `/api/notes/`.