# Work Item Ontology

## Purpose

`Issue / Work / Job / Ticket / Task / TODO / Artifact` を共通語彙として定義し、人間とAgentが同じ仕事モデルを使えるようにする。

## Core model

```text
Issue  ->  Work  ->  Job  ->  Ticket  ->  Task  ->  TODO  ->  Artifact
 WHY      WHAT      EXECUTE    REQUEST      HOW       NEXT       RESULT
```

これは推奨フローであり、すべてのWorkItemが必ず直線的に接続されるという意味ではない。実際の構造はRelationで表現する。

## Concepts

| Type | Meaning | Question |
|---|---|---|
| Issue | 問い・問題・要求 | WHY / WHAT needs solving? |
| Work | 取り組む仕事・活動 | WHAT work are we doing? |
| Job | 実行される処理・役務 | WHAT should a worker/agent execute? |
| Ticket | 実行依頼 | WHAT is requested? |
| Task | 具体的な作業 | HOW? |
| TODO | 最小の次アクション | WHAT next? |
| Artifact | 成果物 | WHAT was produced? |

## Relations

```text
WorkItem
  ├── contains    -> WorkItem
  ├── depends_on  -> WorkItem
  ├── relates_to  -> WorkItem
  ├── requests    -> WorkItem
  ├── executes    -> WorkItem
  ├── verifies    -> WorkItem
  └── produces    -> Artifact
```

`contains` と `depends_on` は別物である。親子関係を依存関係として表現しない。

## Agent model

```text
Human
  |
  v
Issue
  |
  v
Work
  |
  v
Job
  |
  v
Ticket
  |
  v
Task
  |
  v
TODO
  |
  v
Artifact
```

AgentはIssueを観察し、Workを構成し、Jobを実行可能にし、Ticket/Task/TODOへ分解し、Artifactを生成・検証する。

## Status

```text
backlog -> ready -> in_progress -> review -> done
                       |
                       v
                    blocked
                       |
                       v
                     ready
```

不要になったWorkItemは `cancelled` とする。

## GitHub mapping

| Ontology | GitHub representation |
|---|---|
| Issue | GitHub Issue |
| Work | Issue / Project item |
| Job | Issue / workflow job / Agent run |
| Ticket | Issue / Sub-issue |
| Task | Sub-issue / checklist |
| TODO | `- [ ]` checklist |
| Artifact | file / commit / PR / release |

GitHub上のオブジェクト名とOntology上の意味は1対1ではない。Ontologyを意味モデル、GitHubを実装・運用レイヤーとして扱う。

## Example

```text
Issue: myapp MVPを完成させる
  |
  +-- Work: myapp MVP開発
        |
        +-- Job: Hono + HTMX MVPを実装
              |
              +-- Ticket: CRUD APIを追加
                    |
                    +-- Task: items routeを実装
                          |
                          +-- TODO: GET /itemsを書く
                                |
                                +-- Artifact: src/routes/items.ts
```

## Source of truth

機械可読な定義は [`ontology/work-item.yaml`](../ontology/work-item.yaml) とする。
