# FastAPI + MySQL Blog Application

This project is a simple blog application built with FastAPI, SQLAlchemy, and MySQL. It demonstrates basic CRUD operations for users and posts.

## Features
- Create, read, and delete users
- Create, read, and delete posts
- Uses SQLAlchemy ORM for database interactions
- Pydantic models for request validation

## Prerequisites
- Python 3.9+
- MySQL server running locally (default: `localhost:3306`)
- MySQL database named `BlogApplication`
- MySQL user with access (default: `root`/`Ahmadbadar3636`)

## Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd FAST API-MYSQL
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   # Or
   source venv/bin/activate  # On Linux/Mac
   ```

3. **Install dependencies**
   ```bash
   pip install fastapi uvicorn sqlalchemy pymysql
   ```

4. **Configure the database**
   - Make sure your MySQL server is running.
   - Create the database if it doesn't exist:
     ```sql
     CREATE DATABASE BlogApplication;
     ```
   - Update the credentials in `database.py` if needed.

## Running the Application

Start the FastAPI server with Uvicorn:
```bash
uvicorn main:app --reload
```

The API will be available at [http://127.0.0.1:8000](http://127.0.0.1:8000)

## API Endpoints

### Users
- `POST /users/` - Create a new user
- `GET /users/{user_id}` - Get a user by ID

### Posts
- `POST /posts/` - Create a new post
- `GET /posts/{post_id}` - Get a post by ID
- `DELETE /posts/{post_id}` - Delete a post by ID

## Example Requests

### Create a User
```json
POST /users/
{
  "username": "john_doe"
}
```

### Create a Post
```json
POST /posts/
{
  "title": "My First Post",
  "content": "Hello, world!",
  "user_id": 1
}
```

### Get a User
```
GET /users/1
```

### Get a Post
```
GET /posts/1
```

### Delete a Post
```
DELETE /posts/1
```

## API Documentation

Once the server is running, visit [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) for the interactive Swagger UI.

## License

This project is for educational purposes. 