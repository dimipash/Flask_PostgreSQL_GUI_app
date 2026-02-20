# Flask PostgreSQL Profile GUI

A simple Flask web application that displays user profiles stored in a PostgreSQL database. Users can browse through profiles with avatars, bios, countries, and dates of birth.

## Features

- Display user profiles with avatar, name, country flag, bio, and date of birth
- Bottom navigation bar for switching between profiles
- PostgreSQL database integration using psycopg
- Responsive design with clean, modern styling

## Tech Stack

- **Backend**: Flask 3.x
- **Database**: PostgreSQL
- **Driver**: psycopg2-binary
- **Frontend**: HTML/CSS

## Prerequisites

- Python 3.12+
- PostgreSQL database

## Database Setup

Create the `user_profiles` table in your PostgreSQL database:

```sql
CREATE TABLE user_profiles (
    username VARCHAR(50) PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    photo_path VARCHAR(255),
    bio TEXT,
    country VARCHAR(50),
    date_of_birth DATE
);
```

## Configuration

Set the `DATABASE_URL` environment variable with your PostgreSQL connection string:

```bash
export DATABASE_URL="postgresql://user:password@localhost:5432/dbname"
```

## Installation

```bash
pip install -e .
```

## Running the Application

```bash
python app.py
```

The application will start on `http://localhost:8080`.

## Project Structure

```
.
├── app.py              # Main Flask application
├── static/
│   ├── styles.css      # Application styles
│   ├── avatars/        # User avatar images
│   └── flags/          # Country flag images
├── templates/
│   └── index.html      # Profile template
└── pyproject.toml      # Project dependencies
```

## License

MIT
