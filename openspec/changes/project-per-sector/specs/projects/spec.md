# Spec Delta

## Purpose

REST API for managing projects with start date (month/year) and duration (months) with CRUD operations.

## ADDED Requirements

### Requirement: Project belongs to single sector

The system SHALL ensure that each project is assigned to exactly one sector.

#### Scenario: Single sector assignment validated

- **WHEN** a project is created or updated with sector assignment
- **THEN** system validates that project belongs to only one sector and returns appropriate error if multiple sectors assigned

#### Scenario: Multiple sector rejection

- **WHEN** POST/PUT request includes multiple sector assignments for a project
- **THEN** returns 400 with error "Project can only belong to one sector"