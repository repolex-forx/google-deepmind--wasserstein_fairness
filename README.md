# Repolex Knowledge Graph of google-deepmind/wasserstein_fairness

RDF knowledge graph data for [google-deepmind/wasserstein_fairness](https://github.com/google-deepmind/wasserstein_fairness), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/wasserstein_fairness
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── eb4483a2e76f6a3c63bb9019ad1673a6764c80f5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── eb4483a2e76f6a3c63bb9019ad1673a6764c80f5
│           └── chunk-001.nq.gz
├── blob
│   ├── 14156ef956871d52a8c1c25a2298920aa3b08068.nq.gz
│   ├── 19ea3395dd7a3d169cc099d7d313068ebadf7d31.nq.gz
│   ├── 202bd9ea161d7192c0bc3f2b2422929820a7fdb7.nq.gz
│   ├── 7dd56382f9f554f6eea3ad128d389b95aecc97d7.nq.gz
│   ├── 8ec769c597d87d2ca3df3c6877f825888d298ef6.nq.gz
│   ├── 91fd3b1cd0605ba5fb40eae4ba51dc96e5324d56.nq.gz
│   ├── ae805167a58e189f57160deeb3691848a17380f2.nq.gz
│   └── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── eb4483a2e76f6a3c63bb9019ad1673a6764c80f5.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 15 files
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

[google-deepmind/wasserstein_fairness](https://github.com/google-deepmind/wasserstein_fairness)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
