# CI/CD Pipeline Documentation

## Overview

TaskTracker uses GitHub Actions to automate testing, coverage reporting, and Docker image publishing. The workflow runs on pushes to the configured development and feature branches, as well as on pull requests.

---

## Pipeline Stages

### 1. Checkout

The workflow checks out the latest version of the source code.

### 2. Environment Setup

Python 3.12 is installed, and all project dependencies are restored from `requirements.txt`.

### 3. Testing

The complete Pytest test suite is executed against a PostgreSQL 16 service container.

### 4. Coverage

Code coverage is generated using `pytest-cov` to ensure adequate test coverage.

### 5. Image Publishing

After all tests pass, the Docker image is built and pushed to Docker Hub from the configured release branches.

---

## Required Secrets

The following repository secrets must be configured:

* `DOCKERHUB_USERNAME`
* `DOCKERHUB_TOKEN`

---

## Published Image

The latest image is available as:

`<your-dockerhub-username>/tasktracker:latest`

Replace `<your-dockerhub-username>` with your actual Docker Hub username.

---

## Monitoring the Pipeline

Workflow runs and logs are available in the **Actions** tab of the GitHub repository.
