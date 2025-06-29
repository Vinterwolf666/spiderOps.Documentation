---
title: DataController
sidebar_position: 4
---

# `DataController`

Base route: `/Data.Microservice.API/Data`

## `GET /`

Retrieves all data entries from the data store.

**Responses:**
- `200 OK`: List of all `CData` records.
- `400 Bad Request`: Error during retrieval.

---

## `POST /AllDataByID?id={id}`

Retrieves all data entries associated with a specific customer ID.

**Query Parameters:**
- `id` (integer): The ID of the customer.

**Responses:**
- `200 OK`: List of `CData` records.
- `400 Bad Request`: Invalid customer ID or error during retrieval.

---

## `POST /newAccountData`

Creates a new data record for a customer and sends a RabbitMQ notification.

**Query Parameters:**
- `email` (string): Customer's email.
- `subject` (string): Email subject.
- `message` (string): Email body.
- `customerId` (integer): Customer ID.

**Body:** Query-bound `CData` object.

**Responses:**
- `200 OK`: Data added and notification sent.
- `400 Bad Request`: Error during insertion or messaging.

---

## `DELETE /removeAnAccount`

Deletes a customer's data from the store.

**Query Parameters:**
- `email` (string)
- `subject` (string)
- `message` (string)
- `customerId` (integer)

**Responses:**
- `200 OK`: Data deleted successfully.
- `400 Bad Request`: Error during deletion.

---

## `PUT /updateAnAccount`

Updates an existing data record for a customer.

**Query Parameters:**
- `email` (string): Email used for validation or reference.

**Body:** `CData` object with updated values.

**Responses:**
- `200 OK`: Data updated.
- `400 Bad Request`: Error during update.
