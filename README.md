# DaNotes Backend API

This repository contains the backend API for the **DaNotes** application. It is built using **Django** and **Django REST Framework (DRF)** and provides REST endpoints to manage notes.

---

## Tech Stack

- **Framework:** Django
- **API:** Django REST Framework (DRF)
- **Database:** SQLite (Development)

---

## Local Setup

### 1. Clone the repository

```powershell
git clone https://github.com/CWhymann/danotes_backend.git
Set-Location .\danotes_backend\
```

### 2. Create a virtual environment

```powershell
python -m venv .venv
```

### 3. Activate the virtual environment

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Install dependencies

```powershell
pip install -r requirements.txt
```

### 5. Apply database migrations

```powershell
python manage.py migrate
```

### 6. Start the development server

```powershell
python manage.py runserver
```

The API will be available at:

```
http://127.0.0.1:8000/api/
```

---

## API Reference

| Method | Endpoint | Description |
| :----- | :------- | :---------- |
| GET | `/api/notes/` | Retrieve all notes |
| POST | `/api/notes/` | Create a new note |
| GET | `/api/notes/{id}/` | Retrieve a single note |
| PUT | `/api/notes/{id}/` | Update a note |
| DELETE | `/api/notes/{id}/` | Delete a note |

---

## Data Model

The `Note` model contains the following fields:

| Field | Type | Description |
| :---- | :--- | :---------- |
| `id` | Integer | Primary key |
| `title` | CharField | Note title |
| `content` | TextField | Note content |
| `marked` | Boolean | Marks the note as important |
| `trash` | Boolean | Indicates whether the note is in the trash |

---

## Integration

CORS is configured to allow requests from the Angular frontend.

Frontend endpoint:

```
/api/notes/
```

---

## Useful PowerShell Commands

### Create migrations

```powershell
python manage.py makemigrations
```

### Apply migrations

```powershell
python manage.py migrate
```

### Create a superuser

```powershell
python manage.py createsuperuser
```

### Open the Django shell

```powershell
python manage.py shell
```

### Run tests

```powershell
python manage.py test
```

---

## Git Workflow

### Check repository status

```powershell
git status
```

### Stage all changes

```powershell
git add .
```

### Commit changes

```powershell
git commit -m "Implement DaNotes backend API"
```

### Push to GitHub

```powershell
git push origin main
```