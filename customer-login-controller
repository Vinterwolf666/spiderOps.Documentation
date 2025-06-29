---
title: CustomerLogInController
sidebar_position: 1
---

# `CustomerLogInController`

Base route: `/CustomerLogIn.API/CustomerLogIn`

## `POST /LogIn`

Authenticates a customer using their email and password.

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "securepassword"
}
```

**Responses:**
- `200 OK`: Returns an object containing authentication data.
- `400 Bad Request`: Invalid credentials or processing error.

---

## `POST /AllLogInsByCustomerId?id={id}`

Retrieves all login records for a specific customer.

**Query Parameters:**
- `id` (integer): The ID of the customer.

**Responses:**
- `200 OK`: A list of login records.
- `400 Bad Request`: Invalid customer ID.

---

## `POST /ForgetPassword?email={email}`

Sends a password recovery email and publishes an event to RabbitMQ.

**Query Parameters:**
- `email` (string): The registered email address of the customer.

**Responses:**
- `200 OK`: Recovery email sent successfully.
- `400 Bad Request`: Email not found or failed to process.
