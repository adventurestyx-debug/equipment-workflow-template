# Equipment Workflow Template

A generic workflow template for managing equipment issue, return, inspection and audit-relevant tracking.

This repository describes a structured approach for teams that need to know who has which equipment, in what condition, since when, and what still needs to be checked.

## Purpose

Equipment workflows often become unreliable when they are managed through scattered Excel files, informal handovers or incomplete notes.

This template focuses on making responsibility, status and missing information visible.

## Core workflow

### 1. Equipment registration

Every equipment item should have a clear and unique identifier.

Recommended fields:

- Equipment ID
- Equipment name
- Category
- Manufacturer
- Model
- Serial number
- Current status
- Last inspection date
- Comment

### 2. Issue process

When equipment is issued, the process should record who received it and when.

Recommended fields:

- Transaction ID
- Equipment ID
- Issued to
- Issue date
- Planned return date
- Issued by
- Comment

### 3. Return process

When equipment comes back, the return should be documented clearly.

Recommended fields:

- Return date
- Returned by
- Received by
- Missing parts
- Visible damage
- Return comment

### 4. Inspection process

Returned equipment should not automatically become available again.

It should first move into an inspection state until it is checked.

Recommended fields:

- Inspection date
- Inspected by
- Inspection result
- Missing parts confirmed
- Repair required
- Final comment

## Recommended status logic

```text
Available     → equipment is ready for use
Issued        → equipment is currently handed out
In inspection → equipment has returned but is not checked yet
Blocked       → equipment is incomplete, damaged or not ready
Retired       → equipment is no longer in active use
```

## Audit fields

For audit-ready workflows, every relevant transaction should include:

- created at
- created by
- updated at
- updated by
- status before
- status after
- comment or reason
- related equipment ID
- related transaction ID

## Data quality rules

- Equipment IDs must be unique.
- Issue dates and return dates must use a real date format.
- Returned equipment should not become available without inspection.
- Missing parts must be documented.
- Status changes should be traceable.
- Comments should explain exceptions, not replace structured fields.

## Example workflow

```text
Available
   ↓
Issued
   ↓
Returned
   ↓
In inspection
   ↓
Available or Blocked
```

## Principle

```text
If responsibility is not visible, the process is not controlled.
```

## Status

```text
Public workflow template · Generic content · No private business data
```

## Notes

This repository is a public, generic workflow template.

It does not include private source code, company data, technician names, serial numbers or internal implementation details.
