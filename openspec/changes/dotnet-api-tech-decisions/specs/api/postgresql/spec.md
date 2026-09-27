# Spec Delta

## Purpose

PostgreSQL database integration with Entity Framework Core.

## ADDED Requirements

### Requirement: Npgsql provider

The system SHALL use Npgsql as the PostgreSQL provider for Entity Framework Core.

#### Scenario: Npgsql configuration

- **WHEN** adding Npgsql package and configuring DbContext
- **THEN** database connections use PostgreSQL protocol

### Requirement: Connection string configuration

The system SHALL configure connection string in appsettings.json.

#### Scenario: Connection string setup

- **WHEN** configuring PostgreSQL connection in appsettings.json
- **THEN** application connects to database on startup

### Requirement: Database migrations

The system SHALL support Entity Framework Core migrations for PostgreSQL.

#### Scenario: Migration generation

- **WHEN** running `add-migration` command
- **THEN** migration file is generated for schema changes