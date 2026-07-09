# Prompt: Dataset Card

## Purpose

Draft or update a dataset card for a quant workflow dataset.

## Required Inputs

- Dataset name and source.
- Owner and permissions.
- Schema or column summary.
- Dataset grain.
- Date range, frequency, and refresh schedule.
- Timestamp meanings and availability time.
- Known transformations, filters, and quality checks.
- Intended and prohibited uses.

## Prompt

Use the Data Quality Agent and `instructions/data_quality.md`.

Draft a dataset card from this context:

```text
{dataset_context}
```

Return a Markdown dataset card with:

- Dataset overview.
- Source, owner, permissions, and contacts.
- Grain and schema.
- Date range, coverage, frequency, and refresh cadence.
- Lineage and transformations.
- Timestamp semantics and point-in-time availability.
- Missingness, duplicates, stale records, and known caveats.
- Join keys and entity identity notes.
- Intended uses and prohibited uses.
- Validation checks.
- Known risks.
- Open questions.

## Checks

- Distinguish event time, publication time, ingestion time, and availability time when relevant.
- Surface survivorship, restatement, and leakage risks.
- Do not mark unknown fields as resolved.
