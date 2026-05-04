# 🍽️ Food Database API

A RESTful API built using Django and Django REST Framework (DRF) to manage food items.  
This project allows users to perform CRUD operations (Create, Read, Update, Delete) on a food database.

---

## 🚀 Features

- Create new food items  
- Retrieve all food items  
- Retrieve a single food item  
- Update existing food data  
- Delete food items  
- JSON-based REST API  
- Browsable API interface (DRF)

---

## 🛠️ Tech Stack

- Python 3.x  
- Django 5.x  
- Django REST Framework  
- SQLite (default database)  

---

## 📁 Project Structure

FoodDB/
│
├── MongoAPI/              # Main project folder
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   ├── wsgi.py
│
├── Food/                  # App folder
│   ├── __init__.py
│   ├── models.py
│   ├── views.py
│   ├── serializers.py
│   ├── urls.py
│   ├── admin.py
│
├── manage.py
└── README.md

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

git clone https://github.com/your-username/food-db-api.git  
cd food-db-api  

---

### 2. Create Virtual Environment

python -m venv venv  

Activate it:

Windows:
venv\Scripts\activate  

---

### 3. Install Dependencies

pip install -r requirements.txt  

---

### 4. Apply Migrations

python manage.py makemigrations  
python manage.py migrate  

---

### 5. Run Server

python manage.py runserver  

Server will start at:  
http://127.0.0.1:8000/

---

## 🌐 API Endpoints

| Method | Endpoint              | Description              |
|--------|----------------------|--------------------------|
| GET    | /api/foods/          | Get all food items       |
| POST   | /api/foods/          | Create new food item     |
| GET    | /api/foods/<id>/     | Get single food item     |
| PUT    | /api/foods/<id>/     | Update food item         |
| DELETE | /api/foods/<id>/     | Delete food item         |

---

## 📷 Example JSON

### Create Food Item

{
  "name": "Pizza",
  "calories": 300,
  "category": "Fast Food"
}

---

## ⚠️ Common Issues

### 1. TemplateDoesNotExist: rest_framework/api.html

Solution:
- Add 'rest_framework' in INSTALLED_APPS
- Ensure APP_DIRS = True in TEMPLATES

---

### 2. path() missing required argument 'view'

Wrong:
path('home'),

Correct:
path('home/', views.home)

---

## 📌 Future Improvements

- User authentication (JWT)
- Search and filtering
- Pagination
- Deployment (Docker / Cloud)

---

## 🤝 Contributing

Pull requests are welcome.  
For major changes, open an issue first to discuss what you would like to change.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

Your Name  
GitHub: https://github.com/your-username
