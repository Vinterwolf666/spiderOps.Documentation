---
title: PipelinesController
sidebar_position: 6
---

# `PipelinesController`

**Base route:** `/Deployment.Microservice.API.Controllers`

This controller handles the uploading, listing, removal, download, and refinement (using AI) of deployment pipeline YAML files. It plays a key role in automating CI/CD pipelines in the SpiderOps platform.

---

## `GET /DownloadPipeline?id={id}&file_name={file_name}`

Downloads the YAML pipeline file for a given ID.

**Query Parameters:**
- `id` (int): Pipeline ID.
- `file_name` (string): Desired download filename.

**Response:**
- `200 OK`: File stream for download.
- `400 Bad Request`: Error occurred while downloading.

---

## `POST /AllPipelinesByID`

Returns all pipeline configurations associated with a specific customer.

**Request Body/Form Data:**
- `customer_id` (int)

**Response:**
- `200 OK`: List of `Pipelines` objects.
- `400 Bad Request`: Error retrieving records.

---

## `DELETE /RemovePipelinesByID?id={id}`

Deletes a pipeline record by ID.

**Query Parameters:**
- `id` (int): Pipeline ID.

**Response:**
- `200 OK`: Deletion confirmation message.
- `400 Bad Request`: Error deleting pipeline.

---

## `POST /UploadPipeline`

Uploads a new pipeline YAML file and registers it in the database.

**Form Data:**
- `customer_id` (int)
- `yaml_file` (file)
- `cloud` (string)
- `project_language` (string)
- `descriptions` (string)
- `appname` (string)
- `cluster_name` (string)
- `ArtifactRegistryName` (string)
- `REGION` (string)

**Response:**
- `200 OK`: Upload success message.
- `400 Bad Request`: Upload failure.

---

## `POST /RefinePipelineWithAI`

Uses AI (OpenAI GPT) to refine a provided pipeline YAML string.

**Request Body:**
```json
"pipelineContent"
