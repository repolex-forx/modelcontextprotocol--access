# Repolex Knowledge Graph of modelcontextprotocol/access

RDF knowledge graph data for [modelcontextprotocol/access](https://github.com/modelcontextprotocol/access), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/access
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0171db63ebc885ea3574637cb9db7c59792864c3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0171db63ebc885ea3574637cb9db7c59792864c3
│           └── chunk-001.nq.gz
├── blob
│   ├── 0272401a1516bfc1bf071284b98f88e0c3e275ac.nq.gz
│   ├── 0585a31181741171f8793a07508f19ef698f4b6a.nq.gz
│   ├── 08c4c64efc9d4a30bd81a0c48fbdb4179a8ea429.nq.gz
│   ├── 09e8d66a384a653223f62232bcfdcaaf76952943.nq.gz
│   ├── 1354cf1fe1c62771551bcb9b978a9a3a2b53ccec.nq.gz
│   ├── 186b1795b19dcdc32915c8f9d7701bc86e118439.nq.gz
│   ├── 2cb8d6408f6129c301c79cc0835426e00dfde5ff.nq.gz
│   ├── 2f73f4d1384dd65013d606311613726aa10ba137.nq.gz
│   ├── 30c3bb6c4dc85888f21df54c35301e67b02af512.nq.gz
│   ├── 3912d3fc2fba6b99a761db0f3591d5211bc36fe8.nq.gz
│   ├── 3bee1cc30c70d6253db4994c15f83ba3b0fc184e.nq.gz
│   ├── 41784273c9d208bd860f15b23aed31a02b8b6ba1.nq.gz
│   ├── 4ed3ed7cd265111baf7e90e04b60d63a74c56343.nq.gz
│   ├── 5331b9e2262793942fe91ca08af7efd2207a5e21.nq.gz
│   ├── 594c237261ffc9f994e1d69b26fb0019b08aeb53.nq.gz
│   ├── 5efc114fdbb62c6828dceade48ecf0b6f2925ae0.nq.gz
│   ├── 65ea36ea8dae3082fcc149ebf7cc590bd131a5ae.nq.gz
│   ├── 667fee09a516cc2bdb25fdf53f5acc4bfcb52d76.nq.gz
│   ├── 7962d994fb8024b8cf9fe3d8566159fe34eb2083.nq.gz
│   ├── 8e8e1fedc77ee90bb099b703785661489bcf146c.nq.gz
│   ├── 8eccc9c583a2bb86d6208fd795bfa0dc8321b11d.nq.gz
│   ├── 9295c0ed7d16f3f611d15409c3c38c05c4f0feda.nq.gz
│   ├── 942646fc8e7a75007d791b63c3dcd0b362e4ad53.nq.gz
│   ├── 9cf3b8b9d83799dc575870070447a01522805fd9.nq.gz
│   ├── a4736f4034d9923139aa4fb8499a7fb0ee5e2562.nq.gz
│   ├── a744f35280ae4cbd97af037a0cbf119cac8ea71a.nq.gz
│   ├── a95cb0538ce3c313951a42f4a80b55f39421205a.nq.gz
│   ├── b2c570c6f2167bcbe44f87654218ff9524952e17.nq.gz
│   ├── b46bd811d95453f7caa5efddce5620ac5064e221.nq.gz
│   ├── c02840e2170d8c6c113660d5311bb8c52f7b18ff.nq.gz
│   ├── c059af7372ed9bd4089427ec1d5aa2f0ee50d8cd.nq.gz
│   ├── c818dacbd9b6e5700ad0ff9a2aab626117413f93.nq.gz
│   ├── cd560795d2407e4c02e8554229d2fe0ae3057b61.nq.gz
│   ├── d732b3186aa01a9b19e98db33ad02da6536757a6.nq.gz
│   ├── ddead76a15a38c28a250ef126406a571b59648bc.nq.gz
│   └── e21f02e7da47c30c8330d8c61e3516100aff17cb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0171db63ebc885ea3574637cb9db7c59792864c3.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 43 files
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

[modelcontextprotocol/access](https://github.com/modelcontextprotocol/access)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
