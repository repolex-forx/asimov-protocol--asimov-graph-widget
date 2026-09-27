# Repolex Knowledge Graph of asimov-protocol/asimov-graph-widget

RDF knowledge graph data for [asimov-protocol/asimov-graph-widget](https://github.com/asimov-protocol/asimov-graph-widget), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-protocol/asimov-graph-widget
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── eef27529047d7ab951b4bbffb021cad109dbea7e
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── eef27529047d7ab951b4bbffb021cad109dbea7e.nq.gz
│   └── repolex
│       └── eef27529047d7ab951b4bbffb021cad109dbea7e
│           └── chunk-001.nq.gz
├── blob
│   ├── 092408a9f09eae19150818b4f0db5d1b70744828.nq.gz
│   ├── 098833438d8630cf8799f4fe968be30decce27f3.nq.gz
│   ├── 11f02fe2a0061d6e6e1f271b21da95423b448b32.nq.gz
│   ├── 1ffef600d959ec9e396d5a260bd3f5b927b2cef8.nq.gz
│   ├── 2bd5a0a98a36cc08ada88b804d3be047e6aa5b8a.nq.gz
│   ├── 2e79bca0cf8c60ce308f430473cebc8b5af846e8.nq.gz
│   ├── 36b65af1bf40861406961b276db14cd4fe7945e6.nq.gz
│   ├── 42d069eca87e2b34aa737506d3c5963e3508bc7b.nq.gz
│   ├── 4d4c87099ed5a91b97fc157f23feb5b50b2840d4.nq.gz
│   ├── 6f4ac9bcca823100838b88e0b570a28d2fbde6b1.nq.gz
│   ├── 767ed291fdba6920ceb6d43b3cb2dcf5bc101a5a.nq.gz
│   ├── 7d5d2b38d79a39078c97e796ddb11508eb88981d.nq.gz
│   ├── 7ed706bf6ad7f088d658dc7ac794b650c61ff57c.nq.gz
│   ├── 978b02cd40a557837f13c747445664be30b295ee.nq.gz
│   ├── 9f85739e222db83094acebddde915f2168d4b17d.nq.gz
│   ├── a547bf36d8d11a4f89c59c144f24795749086dd1.nq.gz
│   ├── ab2697faf12e43566269ac3a61d550928ddf78ab.nq.gz
│   ├── b36cddc9fc2d8bd0f3217c20c8ba2c02d4b8ee81.nq.gz
│   ├── ce4abdf632ecb75afedc2a30c2fe135431cd668a.nq.gz
│   ├── d1b14cdc822c3d74ee8300b10c7c9201b18e00a7.nq.gz
│   ├── d296490915563f133e751430ed67fac5600ccac2.nq.gz
│   ├── d841fa9dd5be0c6e40a59d3ea94bbdacc9586ab9.nq.gz
│   ├── db0becc8b033a4a78144f4a3bb852082fe91cd62.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f7f5e70fa34f0ec7a902918b0e9c0e737d83856a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── eef27529047d7ab951b4bbffb021cad109dbea7e.nq.gz
├── filetree
│   └── eef27529047d7ab951b4bbffb021cad109dbea7e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 34 files
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

[asimov-protocol/asimov-graph-widget](https://github.com/asimov-protocol/asimov-graph-widget)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
