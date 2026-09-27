# Design

## Context

Enforcing that each project belongs to exactly one sector. The proposal defines the motivation - this design covers the technical approach.

## Goals / Non-Goals

**Goals:**
- Validate single sector assignment on project create/update
- Provide clear error messages for multiple sector assignment
- Maintain data integrity in sector-project relationships

**Non-Goals:**
- Implement specific programming language logic
- Design database schema details
- Modify existing API response formats beyond validation

## Decisions

- Add validation at API layer (POST/PUT /api/projects)
- Return 400 error with clear message if multiple sectors assigned
- Keep existing project structure, only add sector validation

## Risks / Trade-offs

- [Validation may reject valid use cases] → Mitigation: Review sector assignment requirements with stakeholders
- [Future needs may require multi-sector] → Mitigation: Design validation to be extensible, not blocking