# Automate with Django

A practical Django automation project showcasing real-world backend workflows such as:

- CSV-to-database migration
- Database-to-CSV export
- Bulk email sending
- Email tracking (open and click rates)
- Image compression
- Web scraping

## Project Overview

Automate with Django is designed to demonstrate how Django can be used to automate repetitive backend operations commonly found in real-world applications and business workflows.

The project combines data processing, email automation, asynchronous task execution, and scraping utilities into a single Django application.

---

## Features

### CSV to Database Migration
Upload and import CSV files directly into the database using Django models.

### Database to CSV Export
Export database records into downloadable CSV files.

### Bulk Email Sending
Send emails to multiple recipients efficiently using Django email utilities and Celery background tasks.

### Email Tracking
Track:
- Email open rates
- Link click rates

using Sendinblue (Brevo) transactional email services.

### Image Compression
Automatically compress uploaded images to reduce storage size and improve performance.

### Web Scraping
Scrape and extract structured data from websites using BeautifulSoup.

### Background Task Processing
Asynchronous task handling with:
- Celery
- Redis

---

## Tech Stack

- Python
- Django
- Celery
- Redis
- BeautifulSoup4
- SQLite
- CKEditor
- Django Crispy Forms
- Anymail
- Sendinblue (Brevo)

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Ebikemeese/Automate-with-Django.git
cd Automate-with-Django
```

---

### 2. Create a Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Create a `.env` File

Create a `.env` file in the project root and add:

```env
SECRET_KEY=your-secret-key
DEBUG=True

SENDINBLUE_API_KEY=your-sendinblue-api-key

CELERY_BROKER_URL=redis://localhost:6379/0
REDIS_URL=redis://localhost:6379/0

EMAIL_HOST=smtp-relay.brevo.com
EMAIL_PORT=587
EMAIL_HOST_USER=your-email@example.com
EMAIL_HOST_PASSWORD=your-email-password
EMAIL_USE_TLS=True

BASE_URL=http://127.0.0.1:8000
CSRF_TRUSTED_ORIGINS=http://127.0.0.1:8000
```

---

### 5. Apply Migrations

```bash
python manage.py migrate
```

---

### 6. Create Superuser

```bash
python manage.py createsuperuser
```

---

### 7. Run Redis

Make sure Redis is installed and running.

#### Windows
Use:
- Redis for Windows
- Docker
- WSL

#### Linux/macOS

```bash
redis-server
```

---

### 8. Start Celery Worker

```bash
celery -A awd_main worker --loglevel=info
```

---

### 9. Run the Development Server

```bash
python manage.py runserver
```

Open:

```text
http://127.0.0.1:8000
```

---

## Project Structure

```text
Automate-with-Django/
│
├── awd_main/
├── dataentry/
├── uploads/
├── emails/
├── image_compression/
├── stockanalysis/
├── templates/
├── media/
├── static/
├── requirements.txt
├── manage.py
└── .env
```

---

## Example Use Cases

- Automating business data imports
- Email marketing workflows
- Background task processing
- Scraping stock or product data
- Optimizing uploaded media files
- Building backend automation systems

---

## Requirements

- Python 3.10+
- Redis Server
- Internet connection (for email tracking and scraping)

---

## Repository

GitHub Repository:

https://github.com/Ebikemeese/Automate-with-Django.git

---

## Contributing

Contributions, issues, and feature requests are welcome.

Feel free to fork the project and submit a pull request.

---
