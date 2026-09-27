# Proposal

## Why

Define and formalize the technology stack decisions for the .NET REST API project, ensuring consistent choices across the team for framework, dependencies, ORM, testing, and CI/CD pipeline. Currently, technology choices are inconsistent or undocumented, leading to onboarding friction and integration concerns.

## What Changes

- Update design.md with specified technology stack for .NET 8 REST API
- Document technology decisions for team consistency
- Ensure all new projects follow these standardized decisions

## Impact

- All new API projects will use this standardized tech stack
- Development onboarding will follow these documented choices
- CI/CD pipelines will be generated consistent with GitHub Actions setup
- Database migrations will use EF Core with PostgreSQL provider
- Testing strategy will include xUnit unit tests with Moq for mocking and Bogus for data generation