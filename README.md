# Sales Data Storing App - Backend

Backend for the Sales Data Storing App, designed to automate the
storage, validation, and management of sales transactions in a secure
centralized database.

------------------------------------------------------------------------

##  Project Overview

The Sales Data Storing App backend eliminates manual Excel-based sales
recording by:

-   Automatically storing transactions in a relational database
-   Providing secure authentication and role-based access
-   Validating data before persistence
-   Supporting reporting and analytics
-   Ensuring data integrity and reliability (ACID compliant)

This backend is built using **Django** and **PostgreSQL**, with
JWT-based authentication.

------------------------------------------------------------------------

##  Goals

-   Automate sales data entry
-   Reduce human error
-   Provide real-time access to transaction data
-   Ensure security and data integrity
-   Support reporting and analytics

------------------------------------------------------------------------

##  Tech Stack

-   Backend Framework: Django
-   Database: PostgreSQL
-   Authentication: JWT (JSON Web Tokens)
-   Hosting: AWS / Azure / GCP
-   API Type: RESTful API

------------------------------------------------------------------------

##  User Roles

The system supports Role-Based Access Control (RBAC):

-   Front Desk Staff - Create sales entries and view limited records
-   Sales Team - View and search transaction records
-   Management -- Access reporting dashboards and summaries
-   Admin - Full system access and user management

------------------------------------------------------------------------

##  Features

### Core Features

-   Sales data input via API
-   Input validation before saving
-   Secure authentication & authorization
-   Relational database storage (ACID compliant)
-   Error handling with meaningful responses

### Additional Features

-   Sales reporting (daily / weekly / monthly / annual)
-   Search & filter by date, product, or customer
-   Export reports (Excel / PDF)
-   Automated backups

------------------------------------------------------------------------

##  Installation & Setup

### 1️⃣ Clone the Repository

``` bash
git clone <https://github.com/DCIT-321-PROJECT-G-7/sales-manager-backend.git>
cd sales-manager-backend
```

### 2️⃣ Create Virtual Environment

``` bash
python -m venv venv
```

Activate:

Windows:

``` bash
venv\Scripts\activate
```


###  Install Dependencies

``` bash
pip install -r requirements.txt
```

------------------------------------------------------------------------

##  Environment Variables

Create a `.env` file in the root directory:

``` env
SECRET_KEY=your_secret_key
DEBUG=True
DB_NAME=sales_db
DB_USER=postgres
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=5432
JWT_SECRET=your_jwt_secret
```

------------------------------------------------------------------------

##  Database Setup

Create database:

``` sql
CREATE DATABASE salesdb;
```

Run migrations:

``` bash
python manage.py migrate
```


------------------------------------------------------------------------

##  Running the Server

``` bash
python manage.py runserver
```

Server runs at:

http://127.0.0.1:8000/

------------------------------------------------------------------------

##  API Endpoints (Sample)

### Authentication

-   POST /api/auth/login/
-   POST /api/auth/register/
-   POST /api/auth/refresh/

### Sales

-   POST /api/sales/
-   GET /api/sales/
-   GET /api/sales/{id}/
-   PUT /api/sales/{id}/
-   DELETE /api/sales/{id}/

### Reports

-   GET /api/reports/daily/
-   GET /api/reports/weekly/
-   GET /api/reports/monthly/
-   GET /api/reports/export/

------------------------------------------------------------------------

##  Project Structure

    sales-manager-backend/
    │
    ├── sales_app/
    │   ├── models.py
    │   ├── views.py
    │   ├── serializers.py
    │   ├── urls.py
    │   └── permissions.py
    │
    ├── users/
    │   ├── models.py
    │   ├── views.py
    │   └── urls.py
    │
    ├── config/
    │   ├── settings.py
    │   └── urls.py
    │
    ├── manage.py
    ├── requirements.txt
    └── README.md

------------------------------------------------------------------------

##  Security Considerations

-   JWT-based authentication
-   Role-based access control
-   Encrypted sensitive data
-   Input validation and sanitization
-   Secure credentials via environment variables

------------------------------------------------------------------------

##  Performance & Scalability

-   Handles up to 1,000 transactions per day
-   Optimized database indexing
-   Scalable for future POS integration
-   Cloud-ready deployment architecture

------------------------------------------------------------------------



## 📌 License

MIT
