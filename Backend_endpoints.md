---
title: Backend API Index
sidebar_position: 0
---

# 📘 Backend API Endpoints Index

Welcome to the documentation for the backend microservices powering the platform. Here you'll find detailed descriptions and examples for each available controller.

## 🔐 Identity & Authentication Microservice

Handles customer login, logout, account creation, update and password recovery.
- [Customer Login ](customer-login-controller.md)
- [Customer Logout ](customer-logout-controller.md)
- [Customers ](customers-controller.md)

## 🗂️ Data Microservice

Manages user personal data, addresses and contact details.
- [Customers Data ](data-controller.md)

## 🔔 Notifications Microservice

Handles asynchronous email and message delivery via message queues.
- [Notify](notify-controller.md)

## 🚀 Application Deployments

Triggers cloud deployments for containerized applications on GKE.
- [Deploy](deployments-controller.md)

## ⚙️ Pipeline Configuration

Allows uploading, refining and managing GitHub Actions YAML pipelines.
- [pipelines](pipelines-controller.md)

## 📊 Monitoring Deployments

Retrieves real-time performance metrics for deployed applications using GCP Monitoring.
> *[Documentation link pending]*

## 🧪 Deployments Quality

Fetches code quality metrics such as coverage, bugs, vulnerabilities from SonarCloud.
> *[Documentation link pending]*

## 🔐 Deployments Security

Scans for exposed secrets and dependency vulnerabilities using Gitleaks and other tools.
> *[Documentation link pending]*

## 🧩 Extra Microservices Used

- 📫 RabbitMQ: For internal messaging and notifications.
- ☁️ Google Cloud APIs: For interacting with GKE, Artifact Registry, and IAM.
- 🧠 OpenAI: To refine CI/CD pipeline definitions with AI assistance.

---

> For each microservice, detailed endpoint documentation will be linked as it becomes available.
