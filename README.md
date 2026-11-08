# Repolex Knowledge Graph of canonical/karma-k8s-operator

RDF knowledge graph data for [canonical/karma-k8s-operator](https://github.com/canonical/karma-k8s-operator), parsed by [repolex](https://repolex.ai).

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
rlex download canonical/karma-k8s-operator
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 695cabccb38fbe900689776a9de70ddb399450f8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 695cabccb38fbe900689776a9de70ddb399450f8
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b680d508757e960bfc1e7190cc29509514d1562.nq.gz
│   ├── 0cf8aa4551aa28548e77ded41abc64dd747897eb.nq.gz
│   ├── 1527248b125dabe30867ea3750b2a727c6797536.nq.gz
│   ├── 165f36e877ad997dbfcfaafc01120e94f3bb979b.nq.gz
│   ├── 16f1a533f2e39b75a8f40dae954e8b600b4ec8d7.nq.gz
│   ├── 183bcfa596a6302e2010ee816c279904de79862b.nq.gz
│   ├── 1911929481472bb2815c268ee1b3622a45e2f4cd.nq.gz
│   ├── 1bb45e9085b56696c3b53307f0da6268b4b3d16a.nq.gz
│   ├── 1c8f59ed1a24e0b436844a9184de36c5935825e9.nq.gz
│   ├── 1da08a71dede46fc8b9107b1165765486696d7d0.nq.gz
│   ├── 25b5a18d152faed923d99a13bc1c196efe9867b3.nq.gz
│   ├── 400ab77a3f268235d2acfccf328e78eb44f728a4.nq.gz
│   ├── 40c82a3bfd8de35d10bd85073d26a8570c8247fd.nq.gz
│   ├── 47f9caad4f7f8e40c60acd4dbf665ddaa4fba0cd.nq.gz
│   ├── 4a5edabe3b73ddea42cff33919ef0977cff656dc.nq.gz
│   ├── 5baa983a6c37c7c1f04424229cadcec44510410a.nq.gz
│   ├── 6529018230d905782e567630986cf15c86cf441b.nq.gz
│   ├── 652c7d218edf2dc1dcf39f46f745b352c2172801.nq.gz
│   ├── 6993e9bc277af1a72817323bb003e25f0ea5e902.nq.gz
│   ├── 6d8e0b8c79dfe81fb345264f616b9b4160e395a3.nq.gz
│   ├── 76a832c470796c6d9db7f6377e7640df1bd37a8a.nq.gz
│   ├── 7f764c80fb46b6746c20e6bc64066be4e74c7a6d.nq.gz
│   ├── 8200b010af183ff44325a900f6d9c6eca34f7e01.nq.gz
│   ├── 90bd24279c81b0b933bfa4082117fa3ede22bf89.nq.gz
│   ├── b2894c6be71be4e274da896b148c0fc985683167.nq.gz
│   ├── d170442a8b45c936cab80e5489807b9f8579ff1c.nq.gz
│   ├── d579e496f93e6e5175ade3eb3f2a1fa28c04fea7.nq.gz
│   ├── d5e812871b3ae6b4ea26eebfd4a3008da4e316e7.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── d6dcb8608f626f59723c48c5fb7ed2b5e4d17ee3.nq.gz
│   ├── dd0a3c73f7ade0e591520b096d37e8e5862aed58.nq.gz
│   ├── e14ec3435fe24cb798d5b87d79f9d1e30da0a0b1.nq.gz
│   ├── eb255a218f083274aeb7807e4f6fb46b4abe8e02.nq.gz
│   └── ecb9c5d4dc1be385db2e72e14de19905e46093d0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 695cabccb38fbe900689776a9de70ddb399450f8.nq.gz
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

[canonical/karma-k8s-operator](https://github.com/canonical/karma-k8s-operator)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
