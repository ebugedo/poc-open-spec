# Proposal

## Why

Define and formalize the technology stack decisions for the .NET REST API project, ensuring consistent choices across the team for framework, dependencies, ORM, testing, and CI/CD pipeline. Currently, technology choices are inconsistent or undocumented, leading to onboarding friction and integration concerns.

## What Changes

- Update design.md with specified technology stack for .NET 8 REST API
- Add capabilities for each technology component
- Ensure all new projects follow these standardized decisions

## Capabilities

### New Capabilities

- `api/aspnetcore`: .NET 8 ASP.NET Core framework for REST API development
- `api/autofac`: Dependency injection with Autofac container
- `api/swagger`: OpenAPI/Swagger documentation generation
- `api/postgresql`: PostgreSQL database integration
- `api/entityframeworkcore`: ORM with Entity Framework Core
- `api/testing`: Test framework with xUnit, Moq, and Bogus
- `ci-cd/github-actions`: GitHub Actions workflows for CI/CD

### Modified Capabilities

- None - all are new capabilities for this change

## Impact

- All new API projects will use this standardized tech stack
- Development onboarding will follow these documented choices
- CI/CD pipelines will be generated consistent with GitHub Actions setup
- Database migrations will use EF Core with PostgreSQL provider
- Testing strategy will include xUnit unit tests with Moq for mocking and Bogus for data generation