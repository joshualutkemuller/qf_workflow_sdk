# Data Quality Tasks

## Review Dataset

Input: dataset description, schema, sample, date range, and intended use.

Output: data quality review with risks, required checks, and dataset card updates.

## Review Join Plan

Input: source tables, join keys, expected grain, timestamp fields, and filters.

Output: join risk review covering cardinality, nulls, duplicates, entity mapping, and row-count reconciliation.

## Point-In-Time Review

Input: features, labels, timestamps, data availability notes, and prediction horizon.

Output: point-in-time correctness assessment with leakage risks and required validation checks.

## Draft Dataset Card

Input: source description, schema, lineage, quality checks, permissions, and intended uses.

Output: dataset card using the SDK dataset card template.
