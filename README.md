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
│   │   ├── 341bc5c87929b5ae16094a8376a5a417a25eab28
│   │   │   └── chunk-001.nq.gz
│   │   ├── 3b6c8e79ee3c0e17df8121e6486f915ab784437f
│   │   │   └── chunk-001.nq.gz
│   │   ├── 81202733badc6082b8895ff2a1fb252db8042bdb
│   │   │   └── chunk-001.nq.gz
│   │   ├── 8ff1e1a84c3e20074611c229e9834f5efea1d5c7
│   │   │   └── chunk-001.nq.gz
│   │   └── fa47323f8260be431dba064d3c4c9698eb8d5497
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   ├── 341bc5c87929b5ae16094a8376a5a417a25eab28.nq.gz
│   │   ├── 3b6c8e79ee3c0e17df8121e6486f915ab784437f.nq.gz
│   │   └── fa47323f8260be431dba064d3c4c9698eb8d5497.nq.gz
│   └── repolex
│       ├── 3b6c8e79ee3c0e17df8121e6486f915ab784437f
│       │   └── chunk-001.nq.gz
│       └── fa47323f8260be431dba064d3c4c9698eb8d5497
│           └── chunk-001.nq.gz
├── blob
│   ├── 01814c1265b4e1c5e6d44bb5b94847b94cabadc9.nq.gz
│   ├── 04e77dfca0cf471f6bef6c4ec075bec3d5560cbe.nq.gz
│   ├── 095657d8f8aab3bede36844f8bac7743a4b6a2d1.nq.gz
│   ├── 161112d31b2ef8b7679821f491d6a09b05db13de.nq.gz
│   ├── 1e6dbc482dcab4f53090498571f249e09c77b397.nq.gz
│   ├── 21312ca9f3c68ca331914bcd8e30cf144d8b811e.nq.gz
│   ├── 26a04c0eb4eddaee48c35c3bdc64b46c761083ea.nq.gz
│   ├── 309863d6eaf3ac590db8ad68dd33c51fac29040e.nq.gz
│   ├── 31695341ffe2962a7adf865e6e5e85260063fcfa.nq.gz
│   ├── 3c7b0fd13a354412fbb55c61e49eba0f3cbe4d1c.nq.gz
│   ├── 40cca205e88e436b62c5bbc84e791257e8787519.nq.gz
│   ├── 4fffb2f89cbd8f2169ce9914bd16bd43785bb368.nq.gz
│   ├── 53ff29d6950f3616eb0147ee7191bc126c817ba1.nq.gz
│   ├── 561dad30dcf4180e06faba08d095765b9fc480e0.nq.gz
│   ├── 5d08737c0b116976d62703fc6db6bf5731c3e5ba.nq.gz
│   ├── 5d31ef9d8c77c2df9e08d047042c00399e11720f.nq.gz
│   ├── 615453b0459f5bfb9c4a8835bc775f24a4067bcd.nq.gz
│   ├── 69b6a1821724cb5e91ac60337403e5ab77fc8611.nq.gz
│   ├── 6c30e25edf862d4070f157e3f0f14d3b5a8e5238.nq.gz
│   ├── 6ce8745e9cf15a85c31d0d91c0bd76cd6c7cc7af.nq.gz
│   ├── 768448fb72cdf9eae071ea2e693f183f72613132.nq.gz
│   ├── 7d3faeb61033934991f2ee79ec4e968b991703a6.nq.gz
│   ├── 7d6227725994ffacd6382a972b57e8bb1c75efe2.nq.gz
│   ├── 890b09352189eae04fd98d90aa523a2923663cfd.nq.gz
│   ├── 8c16a1378be701592165dbb5a02628ac59e59e5d.nq.gz
│   ├── 90abc4699c5c4c68817eb2d4f6655c78fab53e58.nq.gz
│   ├── 9ea75b977d9f0933705bcf30b640af980b77957a.nq.gz
│   ├── a3bad2cf6b865a22309e910339c41c6c37b6618d.nq.gz
│   ├── b1f3558bb6031571f58d7196507e8659365e30f5.nq.gz
│   ├── bc5c770f3154b9ef6db249af768978c558e9cc16.nq.gz
│   ├── c2f9ce22154037eac6a6f3be8c8f38bc175069fe.nq.gz
│   ├── d2b19cfa28ef763619bfcf8065a054f58aa7d6b2.nq.gz
│   ├── d38f5679abfdf22878dcf794374041bf364bddea.nq.gz
│   ├── d86e215de247eb713cd17f1fea1dd5e9af9d053c.nq.gz
│   ├── d8b8f179e22972f5c24cee521740531d1c04843c.nq.gz
│   ├── daa2777658d53db62d2aca563610447bd020fb46.nq.gz
│   ├── e00beff521c82094b8913eddd4d96813ad42f794.nq.gz
│   ├── e4e76ae4100fb813088fecf5d353799abfc33d2e.nq.gz
│   ├── ee3d2f400dbd82d3679004ce20fecdb2a852b85a.nq.gz
│   ├── f616a7b319e3341941100010eb250206a090d0d5.nq.gz
│   ├── f8169f393d36e191bd66d3b8f87ef4174670ab48.nq.gz
│   ├── fa44b89bdb2c0171197a2968eae2bdbf5804c1cc.nq.gz
│   └── ff7cf59de9f19ad54719f0e347172f3e5460a29f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   ├── 341bc5c87929b5ae16094a8376a5a417a25eab28.nq.gz
│   ├── 3b6c8e79ee3c0e17df8121e6486f915ab784437f.nq.gz
│   └── fa47323f8260be431dba064d3c4c9698eb8d5497.nq.gz
├── filetree
│   ├── 341bc5c87929b5ae16094a8376a5a417a25eab28.nq.gz
│   ├── 3b6c8e79ee3c0e17df8121e6486f915ab784437f.nq.gz
│   ├── 81202733badc6082b8895ff2a1fb252db8042bdb.nq.gz
│   ├── 8ff1e1a84c3e20074611c229e9834f5efea1d5c7.nq.gz
│   └── fa47323f8260be431dba064d3c4c9698eb8d5497.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

20 directories, 66 files
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
*Parsed on 2026-05-10 by [repolex](https://repolex.ai)*
