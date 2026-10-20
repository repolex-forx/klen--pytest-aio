# Repolex Knowledge Graph of klen/pytest-aio

RDF knowledge graph data for [klen/pytest-aio](https://github.com/klen/pytest-aio), parsed by [repolex](https://repolex.ai).

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
rlex download klen/pytest-aio
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 8b54be4cab63ea2b6d74d27ff0ed15838a6366e0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 8b54be4cab63ea2b6d74d27ff0ed15838a6366e0
│           └── chunk-001.nq.gz
├── blob
│   ├── 020bd3fc1bcec6633d069ef41660a3bd61ad2d29.nq.gz
│   ├── 04123739eaed496c8d565bced0c57ffb329c9232.nq.gz
│   ├── 166d72b0683cb67f4ce56245c9637360e0b82ffc.nq.gz
│   ├── 38a1371b02ae449f2c507958e956fd5be34c5eab.nq.gz
│   ├── 4a060cc8ce501e4a5b9157c2f5ed52285582dd60.nq.gz
│   ├── 4d76ea7acb6b40d219d372d82a6e60bb9695046f.nq.gz
│   ├── 69f5532fe7c76117031e9b16ca8470d9e3324efe.nq.gz
│   ├── 73c197b764ee5489902b370c2111676a5f1777ef.nq.gz
│   ├── 74b2f1cafc725c576e69ab123003287fd80a8e05.nq.gz
│   ├── 80e040933592f8ef871a71917b47099e5d63b5d1.nq.gz
│   ├── 85410a1a206bc828920a950f12d98839fca155d6.nq.gz
│   ├── 8d06d62d354f20c05c2b5e6050bf70bac5cce02c.nq.gz
│   ├── 9b01814f39136bbdb53468d6df73cb20d3e29f8d.nq.gz
│   ├── aab20cf480d96816196fd5e6e71cc3b207238815.nq.gz
│   ├── b61a1329aa363b80d1bd54f15c2c873b32248f9a.nq.gz
│   ├── c33abbb909b7f6fd48dcf0a44bf26db9a7005351.nq.gz
│   ├── ca434b77fcfa19b6b8e8dbfc2fff2dc90c9f7cba.nq.gz
│   ├── cac8b9961f5fdc15d71302441f9991872e9c19ec.nq.gz
│   ├── cb1ccd6e13339846c7f9bd8e6daae0b2195aa43b.nq.gz
│   ├── ccabf858487f78743317f70e9ff9eb10fa04ad7c.nq.gz
│   ├── d92189f82a029525dc70418ba26b0e913a7e916c.nq.gz
│   ├── d936cfecec08c2d6a1290ec0b197d0b7f71d6a22.nq.gz
│   ├── dcafe8b5e9620775bbe8563238fc4f57fd7fddeb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f8485cdeecd4ea1eaf96cc05a41e1f7f8fee277e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8b54be4cab63ea2b6d74d27ff0ed15838a6366e0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[klen/pytest-aio](https://github.com/klen/pytest-aio)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
