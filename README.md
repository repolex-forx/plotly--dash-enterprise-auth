# Repolex Knowledge Graph of plotly/dash-enterprise-auth

RDF knowledge graph data for [plotly/dash-enterprise-auth](https://github.com/plotly/dash-enterprise-auth), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/dash-enterprise-auth
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 71f00ab5cc5ee15af59577900d4e72c53bd3e852
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 71f00ab5cc5ee15af59577900d4e72c53bd3e852
│           └── chunk-001.nq.gz
├── blob
│   ├── 07ccac31607bcf5488252f2793c17dc1cdc03f73.nq.gz
│   ├── 218d6dacdd473ba8064558d38c000708a730304e.nq.gz
│   ├── 44b18069b778d38decf1beaf61b6c034ee03d6d5.nq.gz
│   ├── 72c52d62dfb338b7001dc56b88caa0b16188e3ba.nq.gz
│   ├── 894a44cc066a027465cd26d634948d56d13af9af.nq.gz
│   ├── 92d8849887e6abb107025e94c4bf54749dec5eab.nq.gz
│   ├── 9321e6a400d7d50f934323793424f744c574f26d.nq.gz
│   ├── a6a400b93aea6b11f5da26bff9c2cc14f70a8854.nq.gz
│   ├── bb3ec5f0d4c70ef732aa4d399282a5ddb2a008fd.nq.gz
│   ├── bc8371522911dae5c57fa15028a9c84eeb316709.nq.gz
│   ├── c3d642f488298459532a80f4c58b81650967240e.nq.gz
│   ├── dede420a62b8bfd7d03a86e1e0e77b2bcbc259ef.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ea67c9fa12dfed827fd73d563ca304b6a7847114.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 71f00ab5cc5ee15af59577900d4e72c53bd3e852.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 22 files
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

[plotly/dash-enterprise-auth](https://github.com/plotly/dash-enterprise-auth)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
