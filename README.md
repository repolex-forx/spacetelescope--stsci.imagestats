# Repolex Knowledge Graph of spacetelescope/stsci.imagestats

RDF knowledge graph data for [spacetelescope/stsci.imagestats](https://github.com/spacetelescope/stsci.imagestats), parsed by [repolex](https://repolex.ai).

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
rlex download spacetelescope/stsci.imagestats
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ed819da6425473bf3343ab6942182ad0d9b1db15
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ed819da6425473bf3343ab6942182ad0d9b1db15
│           └── chunk-001.nq.gz
├── blob
│   ├── 09966e8a834f2e0fda1e78693c4cffb6f5b9ca2d.nq.gz
│   ├── 10036c8e3246286fd7ed13e5c21f2b9811d12297.nq.gz
│   ├── 17736eac5d9db253ef3cea15f3eb41526aec744d.nq.gz
│   ├── 1d9913122ec7cdd690dddfaec6fd2773fe3956a6.nq.gz
│   ├── 24e816f7e07a00a407f9177b41f72c4fc20557e8.nq.gz
│   ├── 2628d13c6be0b538c6c643fc0a940d7ecb40a057.nq.gz
│   ├── 357fadda4e90c2ad9292230a350b628e505ba7b6.nq.gz
│   ├── 3accd960adfcb575c2b9418c04cc743b2a30ab19.nq.gz
│   ├── 3b1edbf249e673d8fb374266912b845c2b03cae4.nq.gz
│   ├── 41c04d40c60f0c75637c496864284f60030ec140.nq.gz
│   ├── 46596492a6f78ed17e7c802ac53a42e88d229359.nq.gz
│   ├── 536fe2e55d45fd067c2c64c0bb9cf3ad421da451.nq.gz
│   ├── 5dcf5ba2b40c3a43d7119385e6b9d8dfd1ee1ae3.nq.gz
│   ├── 696c71ee7c7a3d2b4c92bb4fe337d06e94abc645.nq.gz
│   ├── 77aa0e49314de28f8d8b91a4a57e3a7bb1758c05.nq.gz
│   ├── 78b5e21cfcc3ac98cb66b3c047df62e15f094e7e.nq.gz
│   ├── 7a5f8a6c7ede351aee5cd038b7f1904de4c103ec.nq.gz
│   ├── 8fc1f5af25952b123b2bf8d2124bc88289556a70.nq.gz
│   ├── 946476a5ef0e3fea061309fc6e33dc74f9e1a45f.nq.gz
│   ├── 96f4ef4b41456570f09e2b1026df28a18a8a578f.nq.gz
│   ├── 98a61118d32ce3aa1e8cd3d97e4a3fa2bf2da903.nq.gz
│   ├── 9d26b7c6b7ed82099e67086799117783ba564fc0.nq.gz
│   ├── a5d7a18115ddcce38de113317259d6e6d7ef84fb.nq.gz
│   ├── ac5ba6cf51da24ac2f9f21a930208b7ddc544089.nq.gz
│   ├── b701ed3aebdbd1b364a4df4cb135af1f28b61913.nq.gz
│   ├── b90f500b493afac104b909db0075ca6e75819f42.nq.gz
│   ├── d04552c08da1d2ffc13e623f7f20828a3d723d1b.nq.gz
│   ├── d349a4303f39608e327b1fb6432086df136c800d.nq.gz
│   ├── d8831475589611c6ac912f7df95c190a21f10ec8.nq.gz
│   ├── e08e23b31efaab443b596b2f1cc4f04dcf7067c2.nq.gz
│   ├── e3763defaedab97d26d65d88e8e1170308b0dcc6.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ebfc6acccab0d10ba8aed9bbd07cb38b0305c113.nq.gz
│   └── f019ef68c38d6575053c6a8c797b82c80e2a5621.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ed819da6425473bf3343ab6942182ad0d9b1db15.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[spacetelescope/stsci.imagestats](https://github.com/spacetelescope/stsci.imagestats)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
