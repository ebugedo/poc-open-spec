# Tasks

## 1. API Setup and Scaffolding

- [ ] 1.1 Initialize Node.js project and install dependencies (express, mongoose, etc.)
- [ ] 1.2 Set up project structure with routes, controllers, and models directories

## 2. Clients Resource

- [ ] 2.1 Create Client model with name, email, and logo fields
- [ ] 2.2 Implement CREATE endpoint for clients (POST /api/clients)
- [ ] 2.3 Implement GET endpoint for single client (GET /api/clients/:id)
- [ ] 2.4 Implement GET endpoint for listing clients (GET /api/clients)
- [ ] 2.5 Implement PUT endpoint for updating client (PUT /api/clients/:id)
- [ ] 2.6 Implement DELETE endpoint for clients (DELETE /api/clients/:id)
- [ ] 2.7 Write and run client unit tests

## 3. Sectors Resource

- [ ] 3.1 Create Sector model with name and description fields
- [ ] 3.2 Implement CRUD endpoints for sectors (POST, GET, PUT, DELETE /api/sectors)
- [ ] 3.3 Write and run sector unit tests

## 4. Projects Resource

- [ ] 4.1 Create Project model with name, startDate (month/year), and duration fields
- [ ] 4.2 Implement end date calculation logic based on start date and duration
- [ ] 4.3 Implement CRUD endpoints for projects (POST, GET, PUT, DELETE /api/projects)
- [ ] 4.4 Implement filtering by start month/year
- [ ] 4.5 Write and run project unit tests

## 5. CI/CD Pipeline

- [ ] 5.1 Set up GitHub Actions workflow for CI
- [ ] 5.2 Configure test script and ensure tests pass
- [ ] 5.3 Set up CD workflow for VPS deployment via SSH
- [ ] 5.4 Create deployment script for VPS (pull, build, restart)
- [ ] 5.5 Add rollback capability to deployment script

## 6. Verification and Documentation

- [ ] 6.1 Run integration tests for all resources
- [ ] 6.2 Generate API documentation
- [ ] 6.3 Test CI/CD pipeline end-to-end