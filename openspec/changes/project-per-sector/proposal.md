# Proposal

## Why

Ensure data integrity by enforcing that each project is assigned to exactly one sector. Currently, the system allows projects to be associated with multiple sectors, which creates ambiguity in reporting and resource allocation.

## What Changes

- Add constraint to project resource: each project must belong to one sector only
- Modify project API validation to enforce single-sector assignment
- Update data model to reflect one-to-many relationship (sector has many projects, project belongs to one sector)

## Capabilities

### New Capabilities

- `data-model/assignments`: Updated relationship between projects and sectors
- `projects`: Modified validation for sector assignment

### Modified Capabilities

- None - all changes are within existing capabilities

## Impact

- Projects endpoint will validate single sector assignment
- Data model updated to reflect cardinality constraint
- Reports and analytics will use correct sector-project mapping