# Spec Delta

## Purpose

CI/CD pipeline configuration for automated deployment to VPS.

## ADDED Requirements

### Requirement: CI pipeline configuration

The system SHALL include a CI pipeline that runs on every push to the main branch.

#### Scenario: CI pipeline trigger

- **WHEN** code is pushed to the main branch
- **THEN** CI pipeline starts and runs tests, builds the artifact

### Requirement: CD pipeline deployment

The system SHALL include a CD pipeline that deploys the application to the VPS after successful CI.

#### Scenario: Successful VPS deployment

- **WHEN** CI pipeline completes successfully
- **THEN** CD pipeline deploys to VPS via SSH and returns 200

### Requirement: Deployment script

The system SHALL have a deployment script that handles the VPS deployment process.

#### Scenario: Deployment script execution

- **WHEN** deployment script is executed
- **THEN** application is restarted, logs are verified, and health check passes

### Requirement: Rollback capability

The system SHALL support rollback to previous version on deployment failure.

#### Scenario: Rollback on failure

- **WHEN** deployment to VPS fails
- **THEN** system rolls back to previous version and restores service