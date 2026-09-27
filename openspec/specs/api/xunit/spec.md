# Spec Delta

## Purpose

Test framework with xUnit, Moq, and Bogus for .NET.

## ADDED Requirements

### Requirement: xUnit test framework

The system SHALL use xUnit as the unit testing framework.

#### Scenario: xUnit test project creation

- **WHEN** creating new xUnit test project
- **THEN** project references main project and can run tests

### Requirement: Moq mocking framework

The system SHALL use Moq for mocking dependencies in tests.

#### Scenario: Moq setup

- **WHEN** setting up mock with `mock.Setup(x => x.Method())`
- **THEN** mock returns configured behavior when called

### Requirement: Bogus data generation

The system SHALL use Bogus for generating test data.

#### Scenario: Bogus data generation

- **WHEN** creating test data with `Faker<>()`
- **THEN** test data is generated with random but deterministic values