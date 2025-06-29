---
title: CustomerLogInController
sidebar_position: 1
---

# `CustomerLogInController`

Ruta base: `/CustomerLogIn.API/CustomerLogIn`

## `POST /LogIn`

Inicia sesión en la plataforma.

**Body:**
```json
{
  "email": "usuario@correo.com",
  "password": "123456"
}
```

**Response:**
- `200 OK`: Datos del cliente autenticado.
- `400 Bad Request`: Credenciales inválidas.

---

## `POST /AllLogInsByCustomerId?id={id}`

Consulta todos los intentos de inicio de sesión de un cliente.

**Query Parameters:**
- `id` (integer): ID del cliente.

**Response:**
- `200 OK`: Lista de objetos `CustomerLogIn`.
- `400 Bad Request`: Si el ID no es válido.

---

## `POST /ForgetPassword?email={email}`

Solicita recuperación de contraseña y envía la solicitud por RabbitMQ.

**Query Parameters:**
- `email` (string): Correo del cliente.

**Response:**
- `200 OK`: Resultado de la solicitud.
- `400 Bad Request`: Si el correo no está registrado.
