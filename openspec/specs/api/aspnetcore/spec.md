# Spec Delta

## Purpose

.NET 8 ASP.NET Core framework for building RESTful APIs.

## ADDED Requirements

### Requirement: ASP.NET Core project structure

The system SHALL use .NET 8 ASP.NET Core Web API project template.

#### Scenario: New project creation with template

- **WHEN** creating a new ASP.NET Core Web API project
- **THEN** project structure includes Controllers, Models, and appsettings.json

### Requirement: Kestrel web server

The system SHALL use Kestrel as the default web server.

#### Scenario: Kestrel server startup

- **WHEN** application starts
- **THEN** Kestrel listens on configured port and returns 200 on health check

### Requirement: Configuration via appsettings.json

The system SHALL use appsettings.json for configuration settings.

#### Scenario: Configuration loading

- **WHEN** application starts
- **THEN** reads configuration from appsettings.json and environment variables