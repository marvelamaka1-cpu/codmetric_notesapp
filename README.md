# Notes API

A RESTful API for managing personal notes, built with Django REST Framework as part of my Codmetric Backend Development internship (Task 1).

## Features

- Full CRUD (Create, Read, Update, Delete) operations for notes
- Built with Django REST Framework
- SQLite database for simplicity
- Structured JSON responses for all endpoints

## Tech Stack

- Python
- Django
- Django REST Framework
- SQLite

## Getting Started

### Prerequisites

- Python 3.x installed
- pip installed

### Installation

1. Clone the repository
```bash
git clone https://github.com/marvelamaka1/codmetric_notesapp.git
cd codmetric_notesapp
```

2. Create and activate a virtual environment
```bash
python -m venv venv
venv\Scripts\activate      # Windows
source venv/bin/activate   # macOS/Linux
```

3. Install dependencies
```bash
pip install django djangorestframework
```

4. Run migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

5. Start the development server
```bash
python manage.py runserver
```

The API will be available at `http://127.0.0.1:8000/api/notes/`

## API Endpoints

| Method | Endpoint            | Description              |
|--------|----------------------|---------------------------|
| GET    | `/api/notes/`         | List all notes            |
| POST   | `/api/notes/`         | Create a new note          |
| GET    | `/api/notes/<id>/`    | Retrieve a single note     |
| PUT    | `/api/notes/<id>/`    | Update a single note       |
| DELETE | `/api/notes/<id>/`    | Delete a single note       |

## Example Request

**Create a note (POST `/api/notes/`)**
```json
{
  "title": "My first note",
  "content": "Testing my Notes API"
}
```

**Response**
```json
{
  "id": 1,
  "title": "My first note",
  "content": "Testing my Notes API",
  "created_at": "2026-07-19T18:00:00Z",
  "updated_at": "2026-07-19T18:00:00Z"
}
```

## Testing

All endpoints were tested using Django REST Framework's browsable API interface, confirming full CRUD functionality.

## Author

**Marvelous Chiamaka Uche**
Backend Development Intern @ Codmetric
[LinkedIn](https://linkedin.com/in/marvelous-chiamaka-096b9874) · [GitHub](https://github.com/marvelamaka1-cpu)

## Acknowledgements

Built as Task 1 of the Codmetric Backend Development Internship.
