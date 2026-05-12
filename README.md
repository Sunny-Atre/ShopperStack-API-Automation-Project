# ShopperStack API Automation Project

> End-to-end API testing suite for the ShopperStack e-commerce platform with bug detection and performance monitoring.

---

## 📌 Project Overview

This project automates the validation of ShopperStack's backend REST APIs — covering user authentication, product browsing, cart management, and order placement. Built using **Postman** with JavaScript assertions.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Postman | API test design and manual execution |
| Newman | CLI-based automated test execution |
| JavaScript | Pre-request scripts and test assertions |
| Newman HTML Reporter | Visual test execution reports |
| Git & GitHub | Version control and project hosting |

---

## 📂 Folder Structure

```
ShopperStack-API-Automation-Project/
├── images/                                      # Screenshots and proof of execution
├── ShopperStack.postman_collection.json         # Postman collection file
├── ShopperStack.postman_environment.json        # Environment variables file
└── README.md                                    # Project documentation
```

---

## 📸 Screenshots

### 1. Postman Collection — Full Test Suite
![Postman Collection](images/postman-collection.png)
> All API requests organized by domain: Auth, Products, Cart, Orders

### 2. Test Assertions — Pass Results
![Test Results](images/test-results.png)
> Green checkmarks confirm status codes, response body fields, and response time validations

### 3. Newman HTML Report — Execution Summary
![Newman Report](images/newman-report.png)
> Auto-generated report showing total tests run, pass/fail breakdown, and per-request response times

### 4. Environment Variables
![Environment Variables](images/env-variables.png)
> Secure token and base URL management using Postman environments

### 5. Sample API Response
![Response Body](images/response-body.png)
> Example JSON response from the login endpoint confirming token generation

---

## ▶️ How to Run

```bash
# Install Newman globally
npm install -g newman

# Install HTML reporter
npm install -g newman-reporter-htmlextra

# Run the collection
newman run ShopperStack.postman_collection.json \
  -e ShopperStack.postman_environment.json \
  -r htmlextra --reporter-htmlextra-export report.html
```

---

## ✅ APIs Tested

| Method | Endpoint | Description |
|--------|----------|-------------|

| POST | /api/auth/login | User login & token generation |
| GET | /api/products | List all products |
| GET | /api/products/:id | Get product by ID |
| POST | /api/cart | Add item to cart |
| PUT | /api/cart/:id | Update cart item quantity |
| DELETE | /api/cart/:id | Remove item from cart |
| POST | /api/orders | Place an order |
| GET | /api/orders/:id | Get order status |

---

## 🐛 Bug Detection

Tests include negative test cases to catch:

- Invalid login credentials returning correct `401` error
- Accessing protected routes without token (expects `403`)
- Adding out-of-stock items to cart
- Response time violations exceeding 2000ms threshold

---

## 👤 Author

**Sunny Atre**
[GitHub Profile](https://github.com/Sunny-Atre)
