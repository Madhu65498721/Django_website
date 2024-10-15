# Django Company Website

This is a simple Django-based website for a company, providing various features such as displaying general company information, services, testimonials, FAQs, a contact form with email integration, and a blog section.

## Features

- **Home Page**: Displays general information about the company, services, testimonials, and recent blog posts.
- **Contact Form**: Users can submit their inquiries, which will be logged and sent via email.
- **Blog**: A section displaying all blog posts and individual blog details.
- **Email Notification**: Sends email notifications for inquiries submitted through the contact form.

## Live Demo

The website is live and can be accessed here: [Live Site](https://madhu5432.pythonanywhere.com/)

## Project Structure

- `views.py`: Contains logic for rendering the homepage, handling contact form submissions, and managing blog posts.
- `models.py`: Defines the database models for general info, services, testimonials, FAQs, contact form logs, and blogs.
- `settings.py`: Configures Django settings, including email backend and database setup.
- `urls.py`: Maps URLs to the corresponding views.
- `templates/`: Contains HTML templates for rendering different pages (index, contact, blog, etc.).
- `static/`: Stores static files like CSS, JavaScript, and images.

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Django 5.1
- Email server configuration (SMTP)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/your-repo.git
   ```

2. Navigate to the project directory:

   ```bash
   cd your-repo
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Apply migrations:

   ```bash
   python manage.py migrate
   ```

5. Run the development server:

   ```bash
   python manage.py runserver
   ```

6. Access the website at `http://127.0.0.1:8000`.

### Environment Variables

To configure email functionality, create a `.env` file in the root directory with the following environment variables:

```
EMAIL_HOST_USER=<your-email>
EMAIL_HOST_PASSWORD=<your-password>
```

## Usage

- **Home Page**: Displays company information and latest blogs.
- **Contact Page**: Users can submit queries that will be logged and emailed.
- **Blogs**: Users can view blog posts and their details.

## Email Configuration

Ensure to configure the email settings in `settings.py` with your SMTP details.

```python
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = os.environ.get('EMAIL_HOST_USER')
EMAIL_HOST_PASSWORD = os.environ.get('EMAIL_HOST_PASSWORD')
```
