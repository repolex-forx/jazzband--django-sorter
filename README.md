# Repolex Knowledge Graph of jazzband/django-sorter

RDF knowledge graph data for [jazzband/django-sorter](https://github.com/jazzband/django-sorter), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/django-sorter
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e92b2f7acc5d331166aa9f7a21a8ce6419bf256f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e92b2f7acc5d331166aa9f7a21a8ce6419bf256f
│           └── chunk-001.nq.gz
├── blob
│   ├── 058672b767091e1f967e6d1bc3e5ce9d2ce69cc7.nq.gz
│   ├── 16a8c5137cde7fd9d85f1a5bcf5481c836dc96cc.nq.gz
│   ├── 2f3a9f8a75144bc5ea3fa8d3219cebe259b42f03.nq.gz
│   ├── 3ca7cc3bea52f8d2b0ff26d00dc5787fc4d3e44c.nq.gz
│   ├── 3e8ba3a644c5312707dc2f4ce58e6259f2846b74.nq.gz
│   ├── 4e546defddccd466ea5b72b28aab3fe4a9586eb9.nq.gz
│   ├── 51e70c373f7fefe525bc551dba23054d34ceff95.nq.gz
│   ├── 522b1b2d6cbe5d3989ea579f434759d4fa4a65ac.nq.gz
│   ├── 5a95d846e57f3c076a20ef70dfa743ed60dce4d2.nq.gz
│   ├── 637cffbc62fdc5942fded0e60daec879a41a5706.nq.gz
│   ├── 6a35e85211133b0a09a81b3962ca871c3e622f88.nq.gz
│   ├── 6cdba0f98e9c0bf208ae78f886669cae43d5d293.nq.gz
│   ├── 710ea2e9eb5ab187385458da0b333bf916440516.nq.gz
│   ├── 875031a975ae80bfb4997221052ca1d4fe5fd922.nq.gz
│   ├── 8899de733fbfe19a10c02c3183c94108d69c2116.nq.gz
│   ├── 8a4521e7b32a50e8bfb89775c69e3643b4987ef1.nq.gz
│   ├── 8de9afca071ef97ade8b0bcc50d836ed9e9084a5.nq.gz
│   ├── a440f7bfe9c047ebbf786f0c7b70fd01d59540e8.nq.gz
│   ├── adfae8cbeda42bd56c3467c9557622faff90b795.nq.gz
│   ├── afaa59aa6ff5fe8204983febd2e3ede3722b0f01.nq.gz
│   ├── b6736b8de88e2c94b053bfd1c48b62672c66d090.nq.gz
│   ├── be515501ac80692bafc7fd71693e7151cc80f989.nq.gz
│   ├── cccf2e8c813a2d02ec1a177cda385caaf37e7569.nq.gz
│   ├── cd0b4a1797fb3b910f9f143a502557b8075cf3f4.nq.gz
│   ├── dc73c84d9d52b35760c42d2dff4f8ee290cc0cac.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f0d91c86349af44bdb2dcf59bba32e5a8297a5d5.nq.gz
│   ├── f76710e58a2665818d31df7cff2a01afdca9b2ef.nq.gz
│   └── fa4e1f4d1715f1d9d01b549d4457cae82d6e2dbf.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e92b2f7acc5d331166aa9f7a21a8ce6419bf256f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[jazzband/django-sorter](https://github.com/jazzband/django-sorter)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
