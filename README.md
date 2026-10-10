# Repolex Knowledge Graph of aio-libs/aiohttp-apischema

RDF knowledge graph data for [aio-libs/aiohttp-apischema](https://github.com/aio-libs/aiohttp-apischema), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiohttp-apischema
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 25d10ce62363fca89dd43d27f2000e9f3213e91d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 25d10ce62363fca89dd43d27f2000e9f3213e91d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b3ebacb0bf7deea8ee9a68b7bfd20d10fc07be3.nq.gz
│   ├── 0b43d6831d39531c9c1ad6d3ae65d2b521240d8e.nq.gz
│   ├── 124541806d8dcc06fa4f6ae01ca75addd1a852fa.nq.gz
│   ├── 1ed45244794b1474c27b511e108b29d3bca6d422.nq.gz
│   ├── 30cb7cae6dd516c51b2d69e8cf10f49093d9ede1.nq.gz
│   ├── 37dc9f632361ae615ad5610bad928a842f3a3e87.nq.gz
│   ├── 3c299eb3fbbb2ed535eef0dd0b195231d64dd359.nq.gz
│   ├── 40e8e793556362d88013c45ad27bc0b689143a88.nq.gz
│   ├── 4b5fead0dc0090c296e74b70f1cca19222ce9a9a.nq.gz
│   ├── 4dde336da398a737ea112939c513cb00d78009a8.nq.gz
│   ├── 515c90ae11d183f521008c28680f2350e9597570.nq.gz
│   ├── 59ca19e9ab3f713a5a8ae74699ef373fba952f71.nq.gz
│   ├── 809bfbe863177c50aa33c8d63479e72cb720b2df.nq.gz
│   ├── 84fbf0817d80e173e6903193475252dc794980e7.nq.gz
│   ├── 92103a47f4dbdf74e601fc914d592b86ff868b2a.nq.gz
│   ├── 9570a7d257fc5c5de793ac8470bfc5dd84ab1551.nq.gz
│   ├── 971b7275c040d7e77dad638dc798462fdafe178f.nq.gz
│   ├── 97c3d5a0fe22dfe4fe840ba414577ef924d5aea8.nq.gz
│   ├── aa1b7c6890ce12f157c74a9114afc87e6cdae9ef.nq.gz
│   ├── ad48605cbc75eaa3cbc28698d93ff7f3df127b5b.nq.gz
│   ├── b2d5e88915001952850ca00e780c027c1f2bfff3.nq.gz
│   ├── b9cbeb678e033a768128cc6444605bc858c51766.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── c69e451cecde08f43afd1f7ee9947832454146ff.nq.gz
│   ├── ca7e8baa3e8610b1cd082195025524154c9bca55.nq.gz
│   ├── d443354602ce02e61008624c46e5deba48720877.nq.gz
│   ├── d9340fb331a4e5b8fab2b4866a0454b2e34be5e4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e6cb0e049729ac0b18fb12b74bca25ea38a70573.nq.gz
│   ├── ef329dd93447a4dd0025f21f7bace637d1be56d4.nq.gz
│   └── f6b68a4694b2feb12c385ed0fd010a12f3befb78.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 25d10ce62363fca89dd43d27f2000e9f3213e91d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[aio-libs/aiohttp-apischema](https://github.com/aio-libs/aiohttp-apischema)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
