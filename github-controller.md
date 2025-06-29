
---
title: Deployment.Github.Controller
sidebar_position: 11
---

# `DeploymentGithubController`
---

## 📌 Base Route

```
/github
```

---

## 📘 Endpoints

### `GET /github/token`

**Description:**  
Retrieves a GitHub token associated with a user.

**Query Parameters:**

| Name   | Type   | Required | Description           |
|--------|--------|----------|-----------------------|
| userId | string | Yes      | The user identifier.  |

**Response:**

```json
{
  "token": "gho_xxxxxx"
}
```

---

### `POST /github/repos`

**Description:**  
Creates a new GitHub repository for a specific user.

**Request Body:**

```json
{
  "userId": "string",
  "repoName": "string"
}
```

**Response:**

```json
{
  "repoUrl": "https://github.com/user/repo-name"
}
```

---

### `POST /github/secrets`

**Description:**  
Adds a secret to a specified GitHub repository.

**Request Body:**

```json
{
  "userId": "string",
  "repoName": "string",
  "secretName": "string",
  "secretValue": "string"
}
```

**Response:**  
`200 OK` on success.

---

### `POST /github/link`

**Description:**  
Links a user's GitHub account using the OAuth authorization code.

**Query Parameters:**

| Name   | Type   | Required | Description                        |
|--------|--------|----------|------------------------------------|
| userId | string | Yes      | The user identifier.               |
| code   | string | Yes      | The OAuth authorization code.      |

**Response:**

```json
{
  "success": true
}
```

---

### `GET /github/link`

**Description:**  
Redirects the user to the GitHub authorization page for account linking.

**Query Parameters:**

| Name        | Type   | Required | Description                                        |
|-------------|--------|----------|----------------------------------------------------|
| userId      | string | Yes      | The user identifier (used as `state` param).       |
| clientId    | string | Yes      | The GitHub OAuth application's client ID.          |
| redirectUri | string | Yes      | The URL to redirect to after authorization.        |

**Response:**  
A redirect (`302 Found`) to GitHub’s OAuth authorization page.

---

## 📦 Data Contracts

### `RepoRequest`

```csharp
public record RepoRequest(string userId, string repoName);
```

### `SecretRequest`

```csharp
public record SecretRequest(string userId, string repoName, string secretName, string secretValue);
```

---

## 🛡️ Notes

- All endpoints assume the existence of a service (`IGithubIntegrationService`) responsible for the business logic.
- OAuth flows and secret storage should follow security best practices (e.g., encrypted storage, token expiration).
