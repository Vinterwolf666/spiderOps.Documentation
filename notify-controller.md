---
title: NotifyController
sidebar_position: 5
---

# `NotifyController`

Base route: `/Customer.Notify.Microservice.API.Notify`

## `GET /AllNotifications`

Returns all notifications available in the system.

**Responses:**
- `200 OK`: List of `Notification` objects.
- `400 Bad Request`: Error while retrieving notifications.

---

## `GET /AllNotificationsByID?id={id}`

Returns all notifications associated with a given customer ID.

**Query Parameters:**
- `id` (integer): Customer ID.

**Responses:**
- `200 OK`: List of notifications.
- `400 Bad Request`: Error retrieving records.

---

## `DELETE /DeleteANotificationById?id={id}`

Deletes a specific notification by its ID.

**Query Parameters:**
- `id` (integer): Notification ID.

**Responses:**
- `200 OK`: Notification deleted.
- `400 Bad Request`: Error during deletion.

---

## `POST /SendNotification`

Sends a new email notification and logs it using RabbitMQ.  
🔒 Requires Authorization.

**Query Parameters:**
- `email` (string)
- `subject` (string)
- `message` (string)
- `customerId` (integer)

**Responses:**
- `200 OK`: Notification sent and RabbitMQ event published.
- `400 Bad Request`: Sending failed.
