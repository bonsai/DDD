# Document Model

**Type:** model
**Status:** accepted
**Source Issues:** #1 #10 #13 #18 #21

A Document is a persistent, reviewable representation of shared knowledge. Its filesystem location is a view; identity and relations are canonical.

## Minimum metadata

`id`, `type`, `status`, `title`, `created`, `updated`, `related_issues`, `relations`, `evidence`, `supersedes`

## Document states

`draft → review → accepted → deprecated / superseded`

Accepted means organizationally adopted knowledge, not metaphysical truth.

## Rule

Documents must expose their sources and downstream consequences. Important decisions must not exist only in chat history.
