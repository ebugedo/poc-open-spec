# Design

## Context

Defining the technology stack for .NET 8 REST API project. The proposal motivates the need for standardized technology choices - this design covers the architectural approach.

## Goals / Non-Goals

**Goals:**
- .NET 8 ASP.NET Core Web API project
- Autofac as DI container
- Swagger/OpenAPI documentation
- PostgreSQL database with EF Core
- xUnit testing with Moq and Bogus
- GitHub Actions CI/CD pipeline

**Non-Goals:**
- Implementation in specific programming languages beyond .NET
- Database schema design details
- Production VPS configuration

## Decisions

- Use .NET 8 LTS as runtime version
- Autofac for DI chosen over built-in .NET Core DI for advanced lifetime management
- Swagger/Gerard chosen for API documentation over custom solution
- PostgreSQL chosen over SQL Server for open-source compatibility
- EF Core with Npgsql provider chosen over raw ADO.NET
- xUnit chosen over NUnit/MSTest for modern .NET testing
- Moq chosen over FakeItEasy/Other for mocking simplicity
- Bogus chosen over hand-crafted test data generators
- GitHub Actions chosen over Azure DevOps/Other for CI/CD given project hosting

## Risks / Trade-offs

- [Learning curve for team unfamiliar with chosen stack] → Mitigation: Documentation and pair programming onboarding
- [PostgreSQL compatibility with existing SQL scripts] → Mitigation: Evaluate migration tooling and test thoroughly
- [Autofac additional overhead vs built-in DI] → Mitigation: Measure performance impact and only use advanced features where needed