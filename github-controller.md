---
title: GithubController
sidebar_position: 9
---

# `GithubController`

**Base route:** `/github`

This controller handles the integration between SpiderOps and GitHub, including OAuth linking, repository creation, and secret injection.

---

## `GET /token?userId=xxx`

Retrieves a stored GitHub access token for a given user.

**Query Parameters:**
- `userId` (string): User's ID.

**Response:**
- `200 OK`: GitHub token string.

---

## `POST /repos`

Creates a GitHub repository under the authenticated user’s account.

**Request Body:**
```json
{
  "userId": "string",
  "repoName": "string"
}
