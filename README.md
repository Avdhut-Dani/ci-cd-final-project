# CI/CD Final Project: Counter Service

This repository contains the RESTful microservice and complete CI/CD automation pipeline for the Coursera course **CI/CD Tools and Practices** (IBM DevOps and Software Engineering Professional Certificate).

## Project Overview

- **Project Name:** CI/CD Final Project - Counter Service Microservice
- **Application:** Python Flask RESTful Counter API
- **Continuous Integration (CI):** Automated linting (`flake8`) and unit tests (`nosetests`) using GitHub Actions.
- **Continuous Deployment (CD):** Cloud-native CI/CD using Tekton and OpenShift Pipelines (`cleanup`, `git-clone`, `flake8`, `nose`, `buildah`, `openshift-client deploy`).
- **Author:** Avdhut Dani

## Usage

This microservice provides endpoints to manage and track counters:
- `GET /` - Root endpoint
- `GET /health` - Health check endpoint returning status 200
- `GET /counters` - List all counters
- `POST /counters/:name` - Create a counter
- `PUT /counters/:name` - Increment a counter
- `DELETE /counters/:name` - Delete a counter

## CI/CD Automation

- **GitHub Actions:** Configured in `.github/workflows/workflow.yml` to automatically checkout the code, install dependencies, run `flake8` linting, and execute unit tests with `nosetests` on every push and pull request to `main`.
- **Tekton & OpenShift Pipelines:** Configured in `.tekton/tasks.yml` to support automated `cleanup` and `nose` unit testing stages within the OpenShift CD pipeline.

## License

Licensed under the Apache License. See [LICENSE](/LICENSE)

## Author

Avdhut Dani (IBM Skills Network Learner)

---
<h3 align="center"> © IBM Corporation. All rights reserved. </h3>
