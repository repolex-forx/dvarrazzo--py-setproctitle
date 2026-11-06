# Repolex Knowledge Graph of dvarrazzo/py-setproctitle

RDF knowledge graph data for [dvarrazzo/py-setproctitle](https://github.com/dvarrazzo/py-setproctitle), parsed by [repolex](https://repolex.ai).

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
rlex download dvarrazzo/py-setproctitle
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2e7124295edef1d84a1e1416290fdeaae9ba6eab
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2e7124295edef1d84a1e1416290fdeaae9ba6eab
│           └── chunk-001.nq.gz
├── blob
│   ├── 0536e3774a15594c168768fc1df2a744bdb8586b.nq.gz
│   ├── 0a93a5c89b4eb1f38b2ede6b68daa7728575f920.nq.gz
│   ├── 1c47bc5d5c1e96a89f274efd17c62315cd09afc9.nq.gz
│   ├── 4078d3666659ec042e43e5e2cb3684392da36423.nq.gz
│   ├── 490d02b4ba88965c78a0ef11701b772dc056a499.nq.gz
│   ├── 4b0b25a7417a35cf9f79ae6ad9826db286778cdf.nq.gz
│   ├── 53034a2c35eb8ab5021ca424017ba2615ddb3ae4.nq.gz
│   ├── 59b9ccc957cbeb22abe0d0368a307043ee57f46f.nq.gz
│   ├── 6290becd72f0f46177a09629264f2b5591133d1c.nq.gz
│   ├── 6d49ca62ef9d2494c616169195f3eeb3bedc6be3.nq.gz
│   ├── 72a34ee6f7eaea95a8d25f9625ede21c4fb11231.nq.gz
│   ├── 83b38e5dd217ac3697dedeefc8f4b50b8f3c2682.nq.gz
│   ├── 8acc36c2d4cd10c851394fc4740b4a520f20df65.nq.gz
│   ├── 8c066ae7d7986ae69a0f5ee1d0bd462e2d550894.nq.gz
│   ├── 8c0f4911fb7b02c25329425ecb469f3f811d3a8f.nq.gz
│   ├── 968f24897b9ffcad043053ab538355e50144ed93.nq.gz
│   ├── 9742c46b0d885998f2db5ef0e859426c3c6cf6de.nq.gz
│   ├── 9ca0076d4b8686ae1e02f9219edf010683e7b729.nq.gz
│   ├── 9e6951bd55b4bea5c1783bd0b89c2f3e17682bae.nq.gz
│   ├── 9fd171a8a74d73572630c1871337aadc93f01584.nq.gz
│   ├── a4a54c197075291930db43b73f6138ab5aa9081f.nq.gz
│   ├── aadb6b3248e8439d871620e202341ef9c5011791.nq.gz
│   ├── b38690948265ea438d06b3278e849aa12997d40c.nq.gz
│   ├── b4d3dfbd9319f2179707ea3afb0c2d65cff67fd4.nq.gz
│   ├── c60f5c7c7b176e617dc6f6dc40bdbebbab1b310f.nq.gz
│   ├── cc3ca219303697893777fdbced6109509420f082.nq.gz
│   ├── d0ad202399fc0c30c9934abbeb728ebde5a4c4a6.nq.gz
│   ├── d16fe6e6d8bd3fe5bf412a2de9c1b9677b55014c.nq.gz
│   ├── da30c07e0d98d30b4c02b2988cc611af824aa895.nq.gz
│   ├── dc8158e72f175a4b17a6dc7595a4a1e3c4d17fdf.nq.gz
│   ├── e51a9c8bf9e2c36f7d057717eabc562b40a296b3.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ef496b28935a383128daca980f6f6565fbab9cf9.nq.gz
│   ├── f1d3b5884b21b7711bb0e9b169731bb53768dfc1.nq.gz
│   ├── f7952275b57496adb34a906d085299cfba729f6d.nq.gz
│   └── fcde77f405f773393360cebd6b40df81b186fe09.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2e7124295edef1d84a1e1416290fdeaae9ba6eab.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 44 files
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

[dvarrazzo/py-setproctitle](https://github.com/dvarrazzo/py-setproctitle)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
