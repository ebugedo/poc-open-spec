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

### Requirement: Project creation

The system SHALL allow creation of a new project with name, start date (month/year), and duration in months.

#### Scenario: Successful project creation

- **WHEN** project data is posted to /api/projects with valid start date and duration
- **THEN** project is created and returns 201 with project data including calculated end date

### Requirement: Project retrieval

The system SHALL allow retrieval of a single project by ID.

#### Scenario: Get project by ID

- **WHEN** GET request is made to /api/projects/{id}
- **THEN** returns 200 with project data

### Requirement: Project filtering by start date

The system SHALL allow filtering projects by start month and year.

#### Scenario: Filter projects by start month

- **WHEN** GET request is made to /api/projects?startMonth=9&startYear=2024
- **THEN** returns 200 with projects starting in September 2024

### Requirement: Project duration validation

The system SHALL validate that duration is a positive integer.

#### Scenario: Invalid duration rejection

- **WHEN** POST request is made to /api/projects with negative duration
- **THEN** returns 400 with validation error

### Requirement: Project end date calculation

The system SHALL calculate and return the project end date based on start date and duration.

#### Scenario: End date calculation

- **WHEN** project created with start date September 2024 and duration 6 months
- **THEN** end date is calculated as March 2025 and returned in response