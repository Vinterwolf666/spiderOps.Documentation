---
title: CustomersController
sidebar_position: 3
---

# `CustomersController`

Base route: `/Customer.Identity.Microservice.Customers.API/Customers`

## `GET /AllCustomers`

Retrieves all customers from the system.

**Responses:**
- `200 OK`: List of all registered customers.
- `400 Bad Request`: Error retrieving customers.

---

## `GET /AllCustomerInfoByID?id={id}`

Returns detailed information about a specific customer.  
🔒 Requires Authorization.

**Query Parameters:**
- `id` (integer): Customer ID.

**Responses:**
- `200 OK`: Customer data.
- `400 Bad Request`: Invalid or non-existent ID.
- `401 Unauthorized`: Token is missing or invalid.

---

## `DELETE /deleteAnAccount?id={id}`

Deletes a customer account.  
🔒 Requires Authorization.

**Query Parameters:**
- `id` (integer): Customer ID.

**Responses:**
- `200 OK`: Account successfully deleted.
- `400 Bad Request`: Error during deletion process.

---

## `POST /newCustomer`

Creates a new customer account and sends a message via RabbitMQ.  
🔒 Requires Authorization.

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "securepassword",
  "firstname": "John",
  "lastname": "Doe"
}
```

**Responses:**
- `200 OK`: Account created successfully.
- `400 Bad Request`: Failed to create account.

---

## `PUT /updateAnAccount`

Updates an existing customer's information.  
🔒 Requires Authorization.

**Request Body:**
```json
{
  "id": 1,
  "email": "updated@example.com",
  "firstname": "John"
}
```

**Responses:**
- `200 OK`: Account updated successfully.
- `400 Bad Request`: Update failed.
