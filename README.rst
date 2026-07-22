Blog Management API
===================

A RESTful Blog Management API built using **FastAPI**, **PostgreSQL**, **SQLAlchemy**, and **JWT Authentication**.

This project provides APIs for user authentication, creating and managing blog articles, comments, profiles, and tags.

The main goal of this project is to demonstrate backend development practices including API design, database management, authentication, authorization, testing, and Docker-based deployment.

Features
--------

* User registration and login
* JWT based authentication
* User profile management
* Create, update, delete and view articles
* Article comments
* Article favorites
* Tags management
* Pagination support
* Database migrations using Alembic
* API documentation using Swagger UI
* Automated testing using Pytest
* Docker support


Technology Stack
----------------

Backend:
    * Python
    * FastAPI
    * SQLAlchemy
    * Pydantic

Database:
    * PostgreSQL

Authentication:
    * JWT Token Authentication

Tools:
    * Docker
    * Alembic
    * Pytest
    * Poetry


Project Setup
-------------

Clone the repository:

::

    git clone https://github.com/sivasankar-rav/blog-management-api.git

Move into the project directory:

::

    cd blog-management-api


Install dependencies:

::

    poetry install


Activate virtual environment:

::

    poetry shell


Environment Configuration
-------------------------

Create a `.env` file in the project root:

::

    APP_ENV=dev
    DATABASE_URL=postgresql://username:password@localhost:5432/blogdb
    SECRET_KEY=your_secret_key


Database Migration
------------------

Run database migrations:

::

    alembic upgrade head


Running the Application
-----------------------

Start the FastAPI server:

::

    uvicorn app.main:app --reload


The application will be available at:

::

    http://localhost:8000


API Documentation
-----------------

Swagger documentation:

::

    http://localhost:8000/docs


ReDoc documentation:

::

    http://localhost:8000/redoc


Running Tests
-------------

Run all tests:

::

    pytest


Project Structure
-----------------

::

    app
    ├── api
    │   ├── routes          - API endpoints
    │   └── dependencies   - API dependencies
    │
    ├── core               - Configuration and security
    │
    ├── db
    │   ├── migrations     - Database migrations
    │   └── repositories   - Database operations
    │
    ├── models             - Database and Pydantic models
    │
    ├── services           - Business logic
    │
    └── main.py            - Application entry point


Docker Deployment
-----------------

Build and start containers:

::

    docker-compose up -d


The API will be available on:

::

    http://localhost:8000


Future Improvements
-------------------

* Add image upload support
* Add role-based authorization
* Add email verification
* Deploy using AWS / Azure
* Add CI/CD pipeline


Author
------

Sivaravula
