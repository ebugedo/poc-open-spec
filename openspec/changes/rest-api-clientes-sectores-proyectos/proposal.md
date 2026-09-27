# Proposal

## Why

Provide a REST API to test and demonstrate the OpenSpec workflow, covering core CRUD operations for business resources (clients, sectors, projects) with CI/CD deployment to a VPS.

## What Changes

- Create REST API with three new resources: clients, sectors, and projects
- Implement CI/CD pipeline configuration for VPS deployment
- Define data models and validation for each resource

## Capabilities

### New Capabilities

- `clients`: REST endpoint for managing clients (including logo attribute) (also usable via gRPC or other mechanisms in the future)
- `sectors`: REST endpoint for managing sectors (also usable via gRPC or other mechanisms in the future)
- `projects`: REST endpoint for managing projects with start date (month/year) and duration (months) (also usable via gRPC or other mechanisms in the future)
- `ci-cd/vps`: CI/CD pipeline configuration for VPS deployment

### Modified Capabilities

- None

## Impact

- New specs under `specs/clients/`, `specs/sectors/`, `specs/projects/`, `specs/ci-cd/vps/`
- Design and tasks for implementation and deployment pipeline