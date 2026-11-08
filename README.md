# Repolex Knowledge Graph of UKPLab/acl2026-expert-rm

RDF knowledge graph data for [UKPLab/acl2026-expert-rm](https://github.com/UKPLab/acl2026-expert-rm), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/acl2026-expert-rm
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 65bcee556c619c3db607df9e96f49da92a04a2ef
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 65bcee556c619c3db607df9e96f49da92a04a2ef
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d03bf268c448d14aeb9becbc045bcde4ae6c9b7.nq.gz
│   ├── 15332e87bcd1bb8730fa06007e1fea856e21e65d.nq.gz
│   ├── 15e5b3df39016c573ea85e522ff659b74ca68113.nq.gz
│   ├── 223387fdbbb54870c1b6473064cf894c4e7b8419.nq.gz
│   ├── 229edba242bb190698662cdce6bdacde9f0769fe.nq.gz
│   ├── 2527d114f734bce044e1f1a5df57a061658e1701.nq.gz
│   ├── 2a54022db9945686a90b75c3bd19e7326ce733e4.nq.gz
│   ├── 3f016cb7a7ff3c31f315e166ae471b73ba75ac49.nq.gz
│   ├── 4da76cce8eaef356b3dfb2f5e32538d9b8c6e6c4.nq.gz
│   ├── 528c925c7c5d8577b572888b38f8dde7888681a1.nq.gz
│   ├── 6f714d634b357a7bc7e5577d9500f59846a4f2f7.nq.gz
│   ├── 73e2c0e4a6b2749dbc0b2873e0aef03192b88406.nq.gz
│   ├── 7bf18a87ce1f1c6cb3990660f49207974ce4c4bb.nq.gz
│   ├── 9b3703a912d40f58fb0fb57d20742e53d9fe7671.nq.gz
│   ├── aa1a0ce247fe4af2c3c3f3c4ce7389e2cd6ccb82.nq.gz
│   ├── c08a79032592be8f5e7318991b0242323389469d.nq.gz
│   ├── c6718de5c5ae59d2c22141a147f5afba41af9cbb.nq.gz
│   ├── d62fc66df4b9acdd5381753fde4173a5775b1ddf.nq.gz
│   ├── daa4859c365585fd7ec65fa3c84abddf5829c32a.nq.gz
│   ├── ea6d05ea8f9d193059c6b06318dbcc5229e7b33a.nq.gz
│   ├── ed3a9d377ba3c30e6eb8b2a35e08e8dc814a0725.nq.gz
│   ├── f00790d440b8fd81259318f9aae85633ba5c8de5.nq.gz
│   └── f9f0632ff2125787a23177768e62e3cd6b6aa013.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 65bcee556c619c3db607df9e96f49da92a04a2ef.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 29 files
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

[UKPLab/acl2026-expert-rm](https://github.com/UKPLab/acl2026-expert-rm)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
