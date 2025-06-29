---
title: DeploymentsController
sidebar_position: 7
---

# `DeploymentsController`

Base route: `/Deployment.Microservice.DEP.API`

## `POST /NewDeployment`

Creates a new deployment request and persists the parameters for later automation.  
🔒 Requires Authorization.

**Query Parameters:**
- Includes repository URL, cluster and registry parameters, app name, language, etc.

**Responses:**
- `200 OK`: Deployment metadata recorded.
- `400 Bad Request`: Input error or failure during setup.

---

## `POST /TriggerDeploymentGCPDeploy`

Triggers the actual GitHub Action + GCP deployment pipeline.  
🔒 Requires Authorization.

**Query Parameters:**
- `repoUrl` (string): URL of the GitHub repository

**Responses:**
- `200 OK`: Pipeline triggered successfully.
- `400 Bad Request`: Error triggering deployment.

---

## `GET /AllGCPDeployByID?id={id}`

Retrieves all GCP deployments associated with a given customer ID.  
🔒 Requires Authorization.

**Query Parameters:**
- `id` (integer): Customer ID

**Responses:**
- `200 OK`: List of deployments
- `400 Bad Request`: Error fetching records

---

## `DELETE /DeleteDeploymentByID?id={id}`

Deletes a deployment record by its internal ID.  
🔒 Requires Authorization.

**Query Parameters:**
- `id` (integer)

**Responses:**
- `200 OK`: Deployment deleted.
- `400 Bad Request`: Error deleting record.
