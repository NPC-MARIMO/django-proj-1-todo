# Django To-Do App

This is a beginner-friendly full-stack Django project for managing to-do tasks. Users can register, log in, and manage their personal to-do lists. The app uses a MySQL database (e.g., Railway) and stores sensitive credentials in a `.env` file.

## Features
- User registration and authentication
- Create, read, update, and delete personal to-dos
- MySQL database support (cloud or local)
- Environment variable support for secrets

## Getting Started

### Prerequisites
- Python 3.8+
- pip
- MySQL database (local or cloud, e.g., Railway)

### Installation
1. **Clone the repository:**
   ```sh
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```
2. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   pip install python-dotenv pymysql
   ```
3. **Create a `.env` file in the project root:**
   ```env
   DB_NAME=your_db_name
   DB_USER=your_db_user
   DB_PASSWORD=your_db_password
   DB_HOST=your_db_host
   DB_PORT=your_db_port
   ```
4. **Apply migrations:**
   ```sh
   python manage.py migrate
   ```
5. **Create a superuser (optional, for admin access):**
   ```sh
   python manage.py createsuperuser
   ```
6. **Run the development server:**
   ```sh
   python manage.py runserver
   ```
7. **Open your browser:**
   Visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## Project Structure
```
myproject/
├── accounts/        # User authentication app
├── todos/           # To-do management app
├── myproject/       # Project settings
├── manage.py
├── .env             # Environment variables (not committed)
├── requirements.txt
└── README.md
```

## Environment Variables
All sensitive data is stored in the `.env` file. **Never commit this file to version control!**

- `DB_NAME`     - Your MySQL database name
- `DB_USER`     - Your MySQL username
- `DB_PASSWORD` - Your MySQL password
- `DB_HOST`     - Your MySQL host (e.g., Railway public host)
- `DB_PORT`     - Your MySQL port (e.g., 3306 or Railway port)

## Useful Commands
- `python manage.py migrate`         # Apply database migrations
- `python manage.py createsuperuser` # Create an admin user
- `python manage.py runserver`       # Start the development server

## License
This project is for learning and personal use. Feel free to modify and share!
