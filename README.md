# Repolex Knowledge Graph of pytest-dev/pytest-base-url

RDF knowledge graph data for [pytest-dev/pytest-base-url](https://github.com/pytest-dev/pytest-base-url), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-base-url
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 538ec4c67be245c6011202df3ff5c3ba84a5a6e9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 538ec4c67be245c6011202df3ff5c3ba84a5a6e9
│           └── chunk-001.nq.gz
├── blob
│   ├── 07f447da8113f1e51ca25e199ad1d66416c88dab.nq.gz
│   ├── 0e0b4504a135976f016b7bf7f88b5e25fbb9cea6.nq.gz
│   ├── 2d9b277ee0c2c312d56b1730301178157bce3594.nq.gz
│   ├── 41dc2327f1698b99dd397a84f47b9596d0a516b5.nq.gz
│   ├── 4baed6826490e85529b727f4d7326cf1afb8240d.nq.gz
│   ├── 66a6c04655660510beda8d45f6508ac0b1489cf0.nq.gz
│   ├── 6c0e54a57a54d607ceaa72f841ad7a26ccf2013b.nq.gz
│   ├── 6c49e8540864e46aa97733dd4b813e6933e2777d.nq.gz
│   ├── 6ed9b083f9b1b4097966a16edc05c4d980aab613.nq.gz
│   ├── 8bcddd9df20a53e52d85c4477301f5f6ec6da2e8.nq.gz
│   ├── a0b0018f2c0c6efac0cf136246495cc36524f6c5.nq.gz
│   ├── b49834e8623b0c8baad2ddd72938360bb8632e56.nq.gz
│   ├── b615121f8916931de9f87dfc9f37e10338c66f3c.nq.gz
│   ├── e5b87e680a4d7bc29ec4c808e23f0cb84d403fe2.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 538ec4c67be245c6011202df3ff5c3ba84a5a6e9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[pytest-dev/pytest-base-url](https://github.com/pytest-dev/pytest-base-url)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
