---
title: QualityController
sidebar_position: 8
---

# `QualityController`

**Base route:** `/Customer.Quality.Microservice.Customers.API/Customers`

This controller manages the interaction with the SonarCloud API to trigger code quality analysis and retrieve code quality metrics associated with a GitHub repository.

---

## `POST /analyze`

Triggers a SonarCloud quality analysis (CI/CD execution simulated or delegated).

**Query Parameters:**
- `gitHubRepoUrl` (string): The URL of the GitHub repository to analyze.
- `sonarProjectKey` (string): The SonarCloud project key.

**Authorization:** Required.

**Response:**
- `200 OK`: Acknowledgment of analysis launch.

---

## `GET /metrics`

Retrieves the latest code quality metrics from SonarCloud for a given project.

**Query Parameters:**
- `sonarProjectKey` (string): The SonarCloud project key.

**Authorization:** Required.

**Response:**
- `200 OK`: A `Quality_iden` object with metrics (e.g., coverage, bugs, vulnerabilities, code smells).
