# 🛒 Ecommerce Product API

A Django REST Framework (DRF) API for managing an e-commerce platform’s products and categories.  
It supports full CRUD operations, product search, ordering, and user authentication.

---

## 🚀 Features

- **Users**
  - User registration and authentication (Django built-in / DRF auth)
- **Categories**
  - Create, read, update, delete categories
- **Products**
  - Create, read, update, delete products
  - Assign products to categories
- **Search & Ordering**
  - Search products by name, description, or category
  - Order products by price or creation date
- **Permissions**
  - Read-only for unauthenticated users
  - Authenticated users can create, update, and delete
- **Pagination**
  - Paginated product lists (default: 10 per page)

---

## 🛠️ Tech Stack

- [Python 3.10+](https://www.python.org/)
- [Django 5](https://www.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)

---

## ⚙️ Installation & Setup

Clone the repository:

```bash
git clone https://github.com/Naoufal1o1/Ecommerce-Product-API.git
cd Ecommerce-Product-API
```

Create and activate a virtual environment:

```bash
python -m venv venv
# Windows PowerShell
venv\Scripts\Activate.ps1
# Git Bash
source venv/Scripts/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Apply migrations:

```bash
python manage.py makemigrations
python manage.py migrate
```

Create a superuser:

```bash
python manage.py createsuperuser
```

Run the server:

```bash
python manage.py runserver
```

The API will be available at:  
👉 http://127.0.0.1:8000/api/

---

## 📚 API Endpoints

### Authentication

- `api-auth/login/` – Login (session based)

### Categories

- `GET /api/categories/` – List categories
- `POST /api/categories/` – Create category
- `GET /api/categories/{id}/` – Retrieve category
- `PUT /api/categories/{id}/` – Update category
- `DELETE /api/categories/{id}/` – Delete category

### Products

- `GET /api/products/` – List products
- `POST /api/products/` – Create product
- `GET /api/products/{id}/` – Retrieve product
- `PUT /api/products/{id}/` – Update product
- `DELETE /api/products/{id}/` – Delete product

### Search & Ordering

- `GET /api/products/?search=phone` – Search products by name, description, or category
- `GET /api/products/?ordering=price` – Order by price (ascending)
- `GET /api/products/?ordering=-price` – Order by price (descending)

---

## 🧪 Example Usage

### Create Category

```json
POST /api/categories/
{
  "name": "Electronics",
  "slug": "electronics"
}
```

### Create Product

```json
POST /api/products/
{
  "name": "iPhone 15",
  "description": "Latest Apple smartphone",
  "price": 1299.99,
  "stock_quantity": 20,
  "image_url": "https://example.com/iphone15.jpg",
  "category_id": 1
}
```

---

## 📦 Deployment

This project can be deployed to:

- [PythonAnywhere](https://www.pythonanywhere.com/)
- [Heroku](https://www.heroku.com/)

## 👨‍💻 Author

**Naoufal Abdelkhalki**  
Backend Engineering Capstone Project – ALX
