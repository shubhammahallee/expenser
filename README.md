# expenser

# 💸 Spendly — Personal Expense Tracker

A full-stack web application built with **Flask** and **SQLite** that helps users track their daily expenses, manage their budget, and understand their spending patterns.

---

## 🚀 Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python 3, Flask |
| Database | SQLite (via Python's built-in `sqlite3`) |
| Frontend | HTML5, CSS3, Jinja2 Templates |
| Testing | pytest, pytest-flask |

---

## 📁 Project Structure

```
expenser/
└── expense-tracker/
    ├── app.py                  # Flask app & all route definitions
    ├── requirements.txt        # Python dependencies
    ├── database/
    │   ├── __init__.py
    │   └── db.py               # DB connection, init, and seed functions
    ├── static/
    │   ├── css/                # Stylesheets
    │   └── js/                 # JavaScript files
    └── templates/
        ├── base.html           # Base layout (extended by all pages)
        ├── landing.html        # Home / landing page
        ├── login.html          # User login page
        └── register.html       # User registration page
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/shubhammahallee/expenser.git
cd expenser/expense-tracker
```

### 2. Create a Virtual Environment

```bash
# Create
python -m venv venv

# Activate — Windows
venv\Scripts\activate

# Activate — macOS/Linux
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Initialize the Database

```bash
python database/db.py
```

> This creates all required SQLite tables using `CREATE TABLE IF NOT EXISTS`.

---

## ▶️ Run the Application

```bash
python app.py
```

Open your browser and go to:

```
http://127.0.0.1:5001/
```

---

## 🌐 Available Routes

| Method | Route | Description |
|--------|-------|-------------|
| GET | `/` | Landing page |
| GET | `/register` | User registration page |
| GET | `/login` | User login page |
| GET | `/logout` | Logout user (in progress) |
| GET | `/profile` | User profile page (in progress) |
| GET | `/expenses/add` | Add a new expense (in progress) |
| GET/POST | `/expenses/<id>/edit` | Edit an expense (in progress) |
| GET | `/expenses/<id>/delete` | Delete an expense (in progress) |

---

## 🧪 Run Tests

```bash
pytest
```

---

## 📌 Notes

- The app runs on port **5001** by default (not the usual 5000).
- `database/db.py` contains three core functions:
  - `get_db()` — returns a SQLite connection with row factory enabled
  - `init_db()` — creates all tables
  - `seed_db()` — inserts sample data for development/testing
- Debug mode is **enabled** — do not use in production.

---

## 👨‍💻 Author

**Shubham Mahallee**  
[GitHub](https://github.com/shubhammahallee)
