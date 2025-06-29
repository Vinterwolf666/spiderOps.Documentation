---
title: CustomerLogOutController
sidebar_position: 2
---

# `CustomerLogOutController`

Base route: `/CustomerLogOut/CustomerLogOut`

## `POST /LogOut?id={id}&token={token}`

Logs a customer out of the system and invalidates their session.

**Query Parameters:**
- `id` (integer): Customer ID.
- `token` (string): Session token.

**Responses:**
- `200 OK`: Successfully logged out.
- `400 Bad Request`: Error processing the logout.

---

## `POST /AllLogOutsByCustomerId?id={id}`

Fetches all logout entries for a specific customer.

**Query Parameters:**
- `id` (integer): Customer ID.

**Responses:**
- `200 OK`: List of logout records.
- `400 Bad Request`: Error retrieving data.
