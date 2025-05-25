# Quiz Master

A Django-based quiz application that allows users to create, take, and manage quizzes.

## Prerequisites

Before you begin, ensure you have the following installed:
- Python 3.8 or higher
- MySQL Server
- phpMyAdmin
- pip (Python package installer)

## Installation Steps

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Quiz-Master
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Database Setup**
   - Open phpMyAdmin (usually at http://localhost/phpmyadmin)
   - Create a new database named `bayanat`
   - The database will be automatically configured with the correct tables when you run migrations

4. **Configure Database Settings**
   The project is already configured to use the following database settings:
   ```python
   DATABASES = {
       'default': {
           'ENGINE': 'django.db.backends.mysql',
           'NAME': 'bayanat',
           'USER': 'root',
           'PASSWORD': '',
           'HOST': 'localhost',
           'PORT': '3306',
       }
   }
   ```
   If your MySQL credentials are different, update them in `core/settings.py`

5. **Run Migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Create Superuser (Admin)**
   ```bash
   python manage.py createsuperuser
   ```
   Follow the prompts to create an admin account

7. **Run the Development Server**
   ```bash
   python manage.py runserver
   ```
   The application will be available at http://127.0.0.1:8000/

## Features

- User authentication and registration
- Quiz creation and management
- Question management
- User dashboard
- Profile management
- Responsive design with Bootstrap 4

## Project Structure

- `core/` - Main project settings
- `users/` - User authentication and profiles
- `quiz/` - Quiz functionality
- `dashboard/` - User dashboard
- `templates/` - HTML templates
- `static/` - Static files (CSS, JS, images)
- `media/` - User-uploaded files

## Troubleshooting

1. **Database Connection Issues**
   - Ensure MySQL server is running
   - Verify database credentials in `core/settings.py`
   - Check if the `bayanat` database exists in phpMyAdmin

2. **Package Installation Issues**
   - If you encounter any issues with `mysqlclient`, you might need to install MySQL Connector C:
     - Windows: Download and install MySQL Connector C from MySQL website
     - Linux: `sudo apt-get install python3-dev default-libmysqlclient-dev build-essential`

3. **Static Files Not Loading**
   - Run `python manage.py collectstatic`
   - Ensure `DEBUG = True` in `core/settings.py`

## Support

For any issues or questions, please open an issue in the repository.

## License

This project is licensed under the MIT License. 