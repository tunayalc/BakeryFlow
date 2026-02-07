# BakeryFlow - Bakery Automation (Flask + MySQL)

BakeryFlow is a small end-to-end bakery ordering system: customer ordering,
admin management, courier delivery, and messaging in a single panel.

Features
- Role-based login: Customer, Admin, Courier
- Order status workflow and logs
- Stock tracking, coupons, favorites, and cart
- Product reviews and messaging

Tech Stack
- Backend: Flask (Python)
- Database: MySQL
- UI: HTML/CSS with Jinja2 templates

Setup
1. Install dependencies:
   pip install -r requirements.txt
2. Create database:
   mysql -u root -p < firin_db.sql
3. Run the app:
   python app.py
   or
   start_firin.bat
4. Open: http://127.0.0.1:5000

Demo Credentials
- Admin: admin / firin
- Customer: musteri1 / 123
- Courier: create from admin panel

Notes
- Demo/learning project.
- DB connection settings are in app.py under db_config.