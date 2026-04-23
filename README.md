# Repolex Knowledge Graph of near/near-gas

RDF knowledge graph data for [near/near-gas](https://github.com/near/near-gas), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download near/near-gas
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3b6c8e79ee3c0e17df8121e6486f915ab784437f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 3b6c8e79ee3c0e17df8121e6486f915ab784437f.nq.gz
│   └── repolex
│       └── 3b6c8e79ee3c0e17df8121e6486f915ab784437f
│           └── chunk-001.nq.gz
├── blob
│   ├── 01814c1265b4e1c5e6d44bb5b94847b94cabadc9.nq.gz
│   ├── 095657d8f8aab3bede36844f8bac7743a4b6a2d1.nq.gz
│   ├── 309863d6eaf3ac590db8ad68dd33c51fac29040e.nq.gz
│   ├── 40cca205e88e436b62c5bbc84e791257e8787519.nq.gz
│   ├── 4fffb2f89cbd8f2169ce9914bd16bd43785bb368.nq.gz
│   ├── 53ff29d6950f3616eb0147ee7191bc126c817ba1.nq.gz
│   ├── 69b6a1821724cb5e91ac60337403e5ab77fc8611.nq.gz
│   ├── 6ce8745e9cf15a85c31d0d91c0bd76cd6c7cc7af.nq.gz
│   ├── 768448fb72cdf9eae071ea2e693f183f72613132.nq.gz
│   ├── 8c16a1378be701592165dbb5a02628ac59e59e5d.nq.gz
│   ├── bc5c770f3154b9ef6db249af768978c558e9cc16.nq.gz
│   ├── d2b19cfa28ef763619bfcf8065a054f58aa7d6b2.nq.gz
│   ├── d8b8f179e22972f5c24cee521740531d1c04843c.nq.gz
│   ├── daa2777658d53db62d2aca563610447bd020fb46.nq.gz
│   ├── e00beff521c82094b8913eddd4d96813ad42f794.nq.gz
│   ├── e4e76ae4100fb813088fecf5d353799abfc33d2e.nq.gz
│   ├── ee3d2f400dbd82d3679004ce20fecdb2a852b85a.nq.gz
│   ├── f616a7b319e3341941100010eb250206a090d0d5.nq.gz
│   └── ff7cf59de9f19ad54719f0e347172f3e5460a29f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 3b6c8e79ee3c0e17df8121e6486f915ab784437f.nq.gz
├── filetree
│   └── 3b6c8e79ee3c0e17df8121e6486f915ab784437f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 29 files
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

## Source repository

[near/near-gas](https://github.com/near/near-gas)

---
*Parsed on 2026-04-23 by [repolex](https://repolex.ai)*
