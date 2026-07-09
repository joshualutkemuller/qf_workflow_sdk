# Example Dataset Card: Analyst Revision Events

## Dataset Overview

Point-in-time analyst estimate revision events used to compute short-horizon revision breadth.

## Source And Permissions

- Source: Placeholder vendor.
- Owner: Research data team.
- Permissions: Internal research use only.

## Grain And Schema

- Grain: One estimate revision event per analyst, security, estimate type, fiscal period, and timestamp.
- Key fields: security identifier, analyst identifier, estimate type, fiscal period, old estimate, new estimate, event timestamp, ingest timestamp.

## Coverage

- Date range: Placeholder.
- Frequency: Event-driven.
- Entity coverage: Liquid US equities with analyst coverage.

## Timestamp Semantics

- Event time: vendor-provided revision timestamp.
- Ingestion time: time the event entered the research warehouse.
- Availability time: must be verified before backtesting.

## Known Risks

- Vendor timestamp may not equal actionable availability time.
- Analyst identifiers may change.
- Historical security mapping must be point-in-time.
- Coverage changes can create selection effects.

## Required Checks

- Compare event timestamp to ingestion timestamp.
- Summarize coverage by date, sector, and market-cap bucket.
- Check duplicate event keys.
- Verify joins to historical security master.
- Confirm that backtest uses availability time, not revised vendor extracts.
