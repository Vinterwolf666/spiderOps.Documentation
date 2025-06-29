
---

### 📄 `monitoring-controller.md`

```markdown
---
title: MonitoringController
sidebar_position: 7
---

# `MonitoringController`

**Base route:** `/Customer.Monitoring.Microservice.Customers.API/Monitoring`

This controller is responsible for fetching real-time or historical metrics related to CPU and cluster status from the deployed GKE clusters associated with each customer.

---

## `GET /metrics/{clusterName}`

Returns a list of monitoring metrics for a specific cluster.

**Path Parameters:**
- `clusterName` (string): GKE cluster name.

**Response:**
- `200 OK`: List of `Monitoring_i` metrics.
- `404 Not Found`: If no metrics are available.

---

## `GET /metrics/CPU/{clusterName}`

Returns CPU-specific monitoring metrics for a cluster.

**Path Parameters:**
- `clusterName` (string): GKE cluster name.

**Response:**
- `200 OK`: List of CPU-related `Monitoring_i` metrics.
- `404 Not Found`: If no CPU metrics are found.
