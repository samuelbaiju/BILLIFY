# Foodie's Hub - Smart Canteen Ordering System

## Objective

**Foodie's Hub** is a smart canteen web application designed to take food orders without standing in any queue. Customers can browse the menu, add items to their cart, and place orders directly from their device. Orders are stored in the admin's database and delivered to the respective tables. The system aims to streamline the food ordering process in canteens and cafeterias.

---

## Features

- **User Authentication:** Sign up, log in, and log out securely.
- **Menu Browsing:** View daily menu items with images, descriptions, and prices.
- **Cart System:** Add, remove, and update items in your cart.
- **Order Placement:** Place orders and select your table number.
- **Bill Summary:** View a detailed bill before confirming your order.
- **Payment:** Cash payment supported (pay at the reception table).  
  _UPI payment integration is in progress._
- **Admin Panel:** Admins can add, edit, and delete menu items and view all orders/bills.
- **Order History:** Users can view their previous bills.

---

## Technologies Used

- **Backend:** Django (Python)
- **Frontend:** HTML5, CSS3, Tailwind CSS, JavaScript
- **Database:** PostgreSQL (or SQLite for development)
- **Deployment:** Render.com
- **Other Libraries:**  
  - `dj-database-url`  
  - `psycopg2-binary`  
  - `gunicorn`  
  - `django-tailwind`  
  - `razorpay` (for future UPI integration)

---

## Project Structure

```
pro/
├── Scripts/
│   └── canweb/
│       ├── canapp/
│       │   ├── templates/
│       │   │   ├── login.html
│       │   │   ├── signup.html
│       │   │   ├── inhome.html
│       │   │   ├── bill_summary.html
│       │   │   ├── view_bills.html
│       │   │   └── ...
│       │   ├── static/
│       │   └── ...
│       ├── canweb/
│       │   ├── settings.py
│       │   └── ...
│       └── requirements.txt
└── ...
```

---

## How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/samuelbaiju/BILLIFY.git
   cd BILLIFY
   ```

2. **Install dependencies:**
   ```bash
   pip install -r Scripts/canweb/requirements.txt
   ```

3. **Apply migrations:**
   ```bash
   python manage.py migrate
   ```

4. **Create a superuser (admin):**
   ```bash
   python manage.py createsuperuser
   ```

5. **Run the development server:**
   ```bash
   python manage.py runserver
   ```

---

## Authentication Details

- **Sign Up:** `/signup/`
- **Log In:** `/login/`
- **Log Out:** `/logout/`
- **Admin Panel:** `/admin/` (for superusers)

---

## Main URLs to Traverse

- **Home (Menu):** `/inhome/`
- **Add Menu (Admin):** `/add-menu/`
- **Edit Menu (Admin):** `/edit-menu/<item_id>/`
- **Delete Menu (Admin):** `/delete-menu/<item_id>/`
- **Add to Cart:** `/add-to-cart/<item_id>/`
- **Remove from Cart:** `/remove-from-cart/<item_id>/`
- **Bill Summary:** `/bill-summary/`
- **View Bills:** `/view-bills/`

> _Note: URLs may vary based on your Django URL configuration._

---

## Payment

- **Cash:** Pay at the reception table after placing your order.
- **UPI:** _Integration in progress. Coming soon!_

---

## Objective Recap

> Take food orders without standing in any queue. Orders are stored in the admin's database and delivered to the tables. Payment via UPI is coming soon; currently, pay at the reception table.

---

## License

This project is for educational/demo purposes.

---
