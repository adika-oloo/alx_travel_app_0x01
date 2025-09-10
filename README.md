Travel App API

A Django REST Framework-based API for managing property listings and bookings. This application provides full CRUD operations for listings and bookings with Swagger documentation.
Features

    Listings Management: Create, read, update, and delete property listings

    Bookings System: Manage bookings for available properties

    RESTful API: Fully compliant with REST standards

    Swagger Documentation: Interactive API documentation

    Authentication Ready: Built-in support for user authentication

API Endpoints
Listings

    GET /api/listings/ - Retrieve all listings

    POST /api/listings/ - Create a new listing

    GET /api/listings/{id}/ - Retrieve a specific listing

    PUT /api/listings/{id}/ - Update a listing

    PATCH /api/listings/{id}/ - Partially update a listing

    DELETE /api/listings/{id}/ - Delete a listing

Bookings

    GET /api/bookings/ - Retrieve all bookings

    POST /api/bookings/ - Create a new booking

    GET /api/bookings/{id}/ - Retrieve a specific booking

    PUT /api/bookings/{id}/ - Update a booking

    PATCH /api/bookings/{id}/ - Partially update a booking

    DELETE /api/bookings/{id}/ - Delete a booking

Installation

    Clone the repository
    bash

git clone https://github.com/yourusername/alx_travel_app_0x01.git
cd alx_travel_app_0x01

Create virtual environment
bash

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Install dependencies
bash

pip install -r requirements.txt

Apply migrations
bash

python manage.py migrate

Create superuser
bash

python manage.py createsuperuser

Run development server
bash

python manage.py runserver

Usage
Accessing the API

    API Base URL: http://localhost:8000/api/

    Swagger Documentation: http://localhost:8000/swagger/

    ReDoc Documentation: http://localhost:8000/redoc/

Testing with Postman

    Get all listings
    text

GET http://localhost:8000/api/listings/

Create a new listing
text

POST http://localhost:8000/api/listings/
Content-Type: application/json

{
  "title": "Beachfront Villa",
  "description": "Luxury villa with ocean view",
  "price": 250.00,
  "bedrooms": 3,
  "bathrooms": 2
}

Update a listing
text

PUT http://localhost:8000/api/listings/1/
Content-Type: application/json

{
  "title": "Updated Villa Name",
  "description": "Updated description",
  "price": 275.00,
  "bedrooms": 3,
  "bathrooms": 2
}

Delete a listing
text

DELETE http://localhost:8000/api/listings/1/

Testing with curl
bash

# Get all listings
curl -X GET http://localhost:8000/api/listings/

# Create a new listing
curl -X POST http://localhost:8000/api/listings/ \
  -H "Content-Type: application/json" \
  -d '{"title": "Mountain Cabin", "description": "Cozy cabin in the woods", "price": 120.00}'

# Update a listing
curl -X PUT http://localhost:8000/api/listings/1/ \
  -H "Content-Type: application/json" \
  -d '{"title": "Updated Cabin", "description": "Renovated cabin", "price": 135.00}'

Project Structure
text

alx_travel_app_0x01/
├── listings/
│   ├── models.py          # Database models
│   ├── serializers.py     # API serializers
│   ├── views.py           # API viewsets
│   ├── urls.py           # Application URLs
│   └── admin.py          # Admin configuration
├── travel_app/
│   ├── settings.py       # Django settings
│   ├── urls.py          # Project URLs
│   └── wsgi.py          # WSGI configuration
├── requirements.txt      # Python dependencies
└── manage.py            # Django management script

Dependencies

    Django==4.2.0

    djangorestframework==3.14.0

    drf-yasg==1.21.5

    Python 3.8+

Contributing

    Fork the repository

    Create a feature branch

    Make your changes

    Add tests for new functionality

    Submit a pull request
