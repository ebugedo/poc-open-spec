# Spec Delta

## Purpose

Entity Framework Core ORM for data access with PostgreSQL.

## ADDED Requirements

### Requirement: DbContext configuration

The system SHALL configure DbContext with PostgreSQL connection via Npgsql.

#### Scenario: DbContext initialization

- **WHEN** application starts and DbContext is created
- **THEN** connection to PostgreSQL database is established

### Requirement: Entity configurations

The system SHALL use entity configurations or Fluent API for entity mapping.

#### Scenario: Entity type configuration

- **WHEN** configuring entity with `.HasKey()` and property mappings
- **THEN** database schema reflects entity structure

### Requirement: LINQ queries

The system SHALL use LINQ for database queries.

#### Scenario: LINQ query execution

- **WHEN** executing LINQ query against DbSet
- **THEN** query is translated to SQL and executed against PostgreSQL