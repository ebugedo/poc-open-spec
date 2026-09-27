# Spec Delta

## Purpose

Dependency injection with Autofac container.

## ADDED Requirements

### Requirement: Autofac container registration

The system SHALL register Autofac as the dependency injection container.

#### Scenario: Autofac container configuration

- **WHEN** application startup configures Autofac container
- **THEN** container is registered and resolves dependencies correctly

### Requirement: Component registration

The system SHALL allow registering components with Autofac.

#### Scenario: Registering services

- **WHEN** services are registered with `builder.RegisterType<>().As<>()`
- **THEN** dependencies can be injected via constructor injection

### Requirement: Lifetime management

The system SHALL support Autofac lifetime management.

#### Scenario: Instance per request

- **WHEN** registering `InstancePerLifetimeScope()`
- **THEN** a new instance is created for each HTTP request