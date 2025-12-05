

# 🐾 PawPal Pet Adaption and Donation App

## Table of Contents
- [Setup](#setup)
- [API Explainantion](#api-explainantion)
- [Sample JSON Response](#sample-json-response)

## Setup

### 1. Install the dependencies
To install the dependencies, run the following command:

```bash
flutter pub get
```
### 2. Install Xampp
### 3. Import the database pawpal_db.sql into Xampp
### 4. Copy API folder to Xampp
### 5. Copy uploads folder to Xampp
### 6. Change IP Address at myconfig.dart
### 5. Run the main.dart file


## API Explainantion
### 1. dbconnect.php
to handle database connection

### 2. login.php
to handle user login and authentication 

### 3. register_user.php    
to handle user registration and ecryption of password and check email already registered or not.

### 4. get_my_pets.php
to load everything about pets and load pets based on search query

### 5. submit_pets.php
to handle submissions of the pets and images of the pets


## Sample JSON Response
### Example of JSON Response for get_my_pets.php
#### ✅ 1. Success Response (With Data)
```json
{
  "status": "success",
  "data": [
    {
      "pet_id": "12",
      "user_id": "5",
      "pet_name": "Buddy",
      "pet_type": "Dog",
      "category": "Lost",
      "description": "Brown dog with a red collar",
      "images_path": "uploads/pets_12_1.png,uploads/pets_12_2.png",
      "lat": "3.12345",
      "lng": "101.54321",
      "created_at": "2025-01-20 15:33:21",
      "name": "Fariz",
      "email": "fariz@example.com",
      "phone": "0123456789",
      "reg_date": "2024-12-01 11:30:05"
    }
  ]
}
```    
#### ✅ 2. Success Response (But No Results Found)
```json
{
    
  "status": "failed",
  "data": []
}
```
### Example of JSON Response for submit_pets.php
#### ✅ 1. Success Response
```json
{
  "status": "success",
  "message": "Pet added successfully"
}
```
#### ❌ 2. Failed Response
```json
{
  "status": "failed",
  "message": "No images provided"
}
```





