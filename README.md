# Repolex Knowledge Graph of twisted/python-info-action

RDF knowledge graph data for [twisted/python-info-action](https://github.com/twisted/python-info-action), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download twisted/python-info-action
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9b0e75d126c6dfb1f0f8703182ebebbdf69e5408
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9b0e75d126c6dfb1f0f8703182ebebbdf69e5408
│           └── chunk-001.nq.gz
├── blob
│   ├── 25d8d3457e71a7e857653704db3b9b666805e43e.nq.gz
│   ├── 487cdc03c5bfd497bbbe3e94e1ef6a3bee18552a.nq.gz
│   ├── 54e8257db2f9a7c2c964e2ae98e065f8e1c1f270.nq.gz
│   ├── 5c327c8f4fd489c3fa6d395665459bea1cb3fc2d.nq.gz
│   ├── ab43c2e330b61b06f958328ba97807d5ee13db77.nq.gz
│   ├── b016e45632c37ae2e1644d3e6c370a29a7ba41d6.nq.gz
│   └── b413b1b5af2a401779e7235b85493c0ed2b71a24.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9b0e75d126c6dfb1f0f8703182ebebbdf69e5408.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 15 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[twisted/python-info-action](https://github.com/twisted/python-info-action)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
