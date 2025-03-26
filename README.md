# Waste Management System

The **Waste Management System** is a Django-based web application designed to streamline waste collection, disposal, and recycling processes. It provides a comprehensive solution for individuals, organizations, and municipal bodies to manage waste efficiently and promote environmental sustainability.

---

## Features

- **User Authentication**: Secure login and registration using JWT (JSON Web Tokens).
- **Waste Collection Tracking**: Schedule and track waste collection in real-time.
- **Recycling Management**: Categorize and manage recyclable materials.
- **PDF Reports**: Generate and export waste management reports in PDF format.
- **Media Management**: Upload and manage media files (e.g., images) using Cloudinary.
- **RESTful APIs**: Built with Django REST Framework (DRF) for seamless integration.
- **PostgreSQL Database**: Reliable and scalable database for structured data storage.
- **Responsive Design**: Accessible on desktop and mobile devices.

---

## Technologies Used

- **Backend**: Django, Django REST Framework (DRF)
- **Database**: PostgreSQL
- **Authentication**: JWT (djangorestframework-simplejwt)
- **Media Storage**: Cloudinary
- **PDF Generation**: xhtml2pdf
- **Static File Handling**: WhiteNoise
- **Production Server**: Gunicorn
- **Dependency Management**: Poetry

---

## Getting Started

### Prerequisites

- Python 3.12 or higher
- PostgreSQL (for database)
- Cloudinary account (for media storage)
- Poetry (for dependency management)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/<your-username>/waste-management.git
   cd waste-management
   ```
2. Install dependencies:
```bash
poetry install
```

3. Set up environment variables:

Create a .env file in the root directory.

Add the following variables:

```bash
SECRET_KEY=your_django_secret_key
DEBUG=True
DATABASE_URL=postgres://user:password@localhost:5432/waste_management
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

4. Run migrations:
```bash
poetry run python manage.py migrate
```
5. Start the development server:
```bash
poetry run python manage.py runserver
```
6. Access the application:

Open your browser and go to http://localhost:8000.
---
API Endpoints

The application provides RESTful APIs for managing waste records, users, and reports. Below are some key endpoints:
---
User Authentication:

POST /api/auth/register/: Register a new user.

POST /api/auth/login/: Log in and obtain JWT tokens.

POST /api/auth/refresh/: Refresh JWT tokens.
---
Waste Management:

GET /api/waste/: Get all waste records.

POST /api/waste/: Add a new waste record.

PUT /api/waste/<id>/: Update a waste record.

DELETE /api/waste/<id>/: Delete a waste record.
---
Reports:

GET /api/reports/: Generate and download waste management reports in PDF format.
---
Deployment
To deploy the application to a production environment:
---
Install Gunicorn:
```bash
poetry add gunicorn
```
7. Collect static files:
```bash
poetry run python manage.py collectstatic
```

8. Run the production server:
```bash
poetry run gunicorn waste_management.wsgi:application
```
9. Deploy to a cloud platform:

Use platforms like Heroku, AWS, or Render for deployment.

10. Configure the DATABASE_URL and CLOUDINARY credentials in the production environment.

---

Contributing
We welcome contributions! If you'd like to contribute to this project, please follow these steps:

Fork the repository.

Create a new branch:

```bash
git checkout -b feature/your-feature-name
```
Commit your changes:
```bash
git commit -m "Add your feature"
```
Push to the branch:
```bash
git push origin feature/your-feature-name
```
Open a pull request.
---
License
This project is licensed under the MIT License. See the LICENSE file for details.
---
Contact
For any questions or feedback, feel free to reach out:
---
Name: Pratik Rakhonde

Email: pratikrakhonde26@gmail.com

GitHub: https://github.com/pratik26x
---
Acknowledgments

Thanks to the Django and Django REST Framework communities for their excellent documentation and support.

Special thanks to Cloudinary for providing media storage solutions.

Inspired by global efforts to promote sustainability and efficient waste management.


---

![Demo](demo.gif)
## Features
- Real-time waste tracking
- AI-powered sorting

---

### **How to Use This README**
1. Copy the entire content above.
2. Paste it into a file named `README.md` in the root directory of your project.
3. Replace placeholders (e.g., `your-username`, `your_django_secret_key`, `your_cloudinary_cloud_name`) with actual values.
4. Add actual screenshots, logos, or additional sections as needed.
5. Commit and push the `README.md` file to your GitHub repository.

---


