# Spec Delta

## Purpose

REST API for managing sectors with CRUD operations.

## ADDED Requirements

### Requirement: Sector creation

The system SHALL allow creation of a new sector with name and description.

#### Scenario: Successful sector creation

- **WHEN** sector data is posted to /api/sectors
- **THEN** sector is created and returns 201 with sector data

### Requirement: Sector retrieval

The system SHALL allow retrieval of a single sector by ID.

#### Scenario: Get sector by ID

- **WHEN** GET request is made to /api/sectors/{id}
- **THEN** returns 200 with sector data

### Requirement: Sector listing

The system SHALL allow listing all sectors with pagination.

#### Scenario: List sectors

- **WHEN** GET request is made to /api/sectors?page=1&limit=10
- **THEN** returns 200 with paginated sector list

### Requirement: Sector update

The system SHALL allow updating sector information.

#### Scenario: Update sector

- **WHEN** PUT request is made to /api/sectors/{id} with new data
- **THEN** sector is updated and returns 200 with updated data

### Requirement: Sector deletion

The system SHALL allow deletion of a sector.

#### Scenario: Delete sector

- **WHEN** DELETE request is made to /api/sectors/{id}
- **THEN** returns 204 and sector is removed