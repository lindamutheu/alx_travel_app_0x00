# alx_travel_app_0x00

> Django-based travel listing application focused on database modeling, serialization, and data seeding.

## 📚 Project Objective

This project demonstrates how to:
- Define Django database models with appropriate relationships and constraints.
- Create serializers for RESTful API representation.
- Seed the database with sample data using a custom Django management command.

---

## 🚀 Getting Started

### 🔁 1. Duplicate Project

This project is a duplicate of `alx_travel_app`, renamed to `alx_travel_app_0x00`.

---

### 🏗️ 2. Models

Defined in `listings/models.py`:

- **Listing (Property):** Contains property details like name, host, price per night, etc.
- **Booking:** Stores user booking data with status and date range.
- **Review:** User ratings and comments for listings, limited to one review per user per listing.

Each model includes:
- Proper field types and constraints (e.g., UUIDs, check constraints, unique constraints)
- Foreign key relationships with Django’s `User` model

---

### 📦 3. Serializers

Defined in `listings/serializers.py`:

- `ListingSerializer`: Handles serialization of `Listing` model
- `BookingSerializer`: Handles serialization of `Booking` model

These serializers are used for converting model instances into JSON format and vice versa.

---

### 🌱 4. Data Seeding

A custom management command is created to populate the database with sample data.

- **Location:**  
  `listings/management/commands/seed.py`

- **Command to run:**  
  ```bash
  python manage.py seed
