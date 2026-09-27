# Proposal

## Why

Provide a REST API to test and demonstrate the OpenSpec workflow, covering core CRUD operations for business resources (clients, sectors, projects) with CI/CD deployment to a VPS.

## What Changes

- Create REST API with three new resources: clients, sectors, and projects
- Implement CI/CD pipeline configuration for VPS deployment
- Define data models and validation for each resource

## Capabilities

### New Capabilities

- `api/clients`: REST endpoint for managing clients (including logo attribute)
- `api/sectors`: REST endpoint for managing sectors
- `api/projects`: REST endpoint for managing projects with start date (month/year) and duration (months)
- `ci-cd/vps`: CI/CD pipeline configuration for VPS deployment

### Modified Capabilities

- None

## Impact

- New specs under `specs/api/clients/`, `specs/api/sectors/`, `specs/api/projects/`, `specs/ci-cd/vps/`
- Design and tasks for API implementation and deployment pipeline