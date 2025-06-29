---
title: GCPInfrastructureController
sidebar_position: 6
---

# `GCPInfrastructureController`

Base route: `/Customer.Infrastructure.Microservice.Infrastructure.API`

## `POST /AllInfrastructureByID`

Returns a list of all infrastructure resources associated with a specific customer ID.

**Query Parameters:**
- `id` (integer): Customer ID

**Responses:**
- `200 OK`: List of infrastructure records.
- `400 Bad Request`: Error fetching data.

---

## `GET /NewInfrastructure`

Creates a new GCP infrastructure setup and triggers a RabbitMQ notification.  
🔒 Requires Authorization.

**Query Parameters:**
- `customer_id` (int)
- `language` (string)
- `template` (string)
- `id` (int)
- `REGION`, `CLUSTER_NAME`, `ARTIFACT_REGISTRY_REGION`, `ARTIFACT_REGISTRY`, `APP_NAME` (strings)

**Responses:**
- `200 OK`: Infrastructure provisioned.
- `404 Not Found`: Template not found.
- `400 Bad Request`: Error during creation.

---

## `DELETE /RemoveInfrastructureByID?id={id}`

Deletes a specific infrastructure record by ID.

**Query Parameters:**
- `id` (integer)

**Responses:**
- `200 OK`: Infrastructure removed.
- `400 Bad Request`: Error during deletion.
