# Repolex Knowledge Graph of argilla-io/python-elasticsearch-runner

RDF knowledge graph data for [argilla-io/python-elasticsearch-runner](https://github.com/argilla-io/python-elasticsearch-runner), parsed by [repolex](https://repolex.ai).

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
rlex download argilla-io/python-elasticsearch-runner
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5a6537c5bffef4d5e53a729ceb7aca102209345d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5a6537c5bffef4d5e53a729ceb7aca102209345d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0511eed6c4543a3b7edbd0b0328529f1d71b0c8e.nq.gz
│   ├── 051bba3b861d3a141aaea9b6bcc8d67a5107cad3.nq.gz
│   ├── 16a0469f74da94868f32156382d211d8e42fb298.nq.gz
│   ├── 1ae04bdb130921c67e749aa9648892e08c697a14.nq.gz
│   ├── 49cee5c6acb59d1580cf701cf93dfeff86214c5f.nq.gz
│   ├── 4c23180bd7ec78c2812052fe344ede51e235597c.nq.gz
│   ├── 509693849ffa6c19f7a9b90f44af23e909ad42c0.nq.gz
│   ├── 75b4ca2fd2d6139b29c555c37f075ef2fcf158ad.nq.gz
│   ├── 939aa1eed0ef7c035b173d8ea0905743b618f9d1.nq.gz
│   ├── 94a88cad554f34366b9c60a6061c9676727b2977.nq.gz
│   ├── 9c8e922c04a9603e7393069074221e879b1bce80.nq.gz
│   ├── a1d66893f1c415f286d7b57800f3a705466e3320.nq.gz
│   ├── d4468fa240250f635381d5da50f6ecec2d2c0eb1.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f154e50eec3e41170ca94e24fab4bf555cbda3da.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5a6537c5bffef4d5e53a729ceb7aca102209345d.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 22 files
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

[argilla-io/python-elasticsearch-runner](https://github.com/argilla-io/python-elasticsearch-runner)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
