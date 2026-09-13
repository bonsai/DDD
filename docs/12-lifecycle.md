# Lifecycle

**Type:** lifecycle
**Status:** accepted
**Source Issues:** #6 #13 #15

Issue and Document have separate state machines.

## Issue

`open → investigating → proposed → resolved / closed`

An Issue may be reopened when new evidence invalidates the resolution.

## Document

`draft → review → accepted → deprecated / superseded`

## Decision rule

An ADR becomes authoritative only when accepted. A superseded document remains in the lineage and is not deleted.

## Feedback loop

Release and operation produce Feedback. Feedback may update Documents or create new Issues.
