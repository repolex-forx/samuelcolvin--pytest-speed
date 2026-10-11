# Repolex Knowledge Graph of samuelcolvin/pytest-speed

RDF knowledge graph data for [samuelcolvin/pytest-speed](https://github.com/samuelcolvin/pytest-speed), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/pytest-speed
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 21b84fa1ae64c4616cb681551378688e7d18161d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 21b84fa1ae64c4616cb681551378688e7d18161d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0236a25979a7f0663542e7083df868208ee9e239.nq.gz
│   ├── 242360d85234cf912505d9514d6c75db52d33178.nq.gz
│   ├── 39fd7ae421f3762ee16b628c4e8187c025ca6089.nq.gz
│   ├── 4d2f89a74804fd67a1d2c2bfeecdad32ff0b0a3d.nq.gz
│   ├── 53588569dd718848aec1fadd43edeb1197b8fb2e.nq.gz
│   ├── 5b417432df90728cc8a86939e99e2c1fe6091663.nq.gz
│   ├── 5d92b718bbafe597398dd60883288ad8f33b76cc.nq.gz
│   ├── 62c7eb8f7ae00e4e3d4fc8a9636815a141e57491.nq.gz
│   ├── 6663a345eea237603d601b8274acda0f53287cc0.nq.gz
│   ├── 684296658577cfe5712e01d359c380b7705f7b4f.nq.gz
│   ├── 70d8b3c5e316a3de3f74cd1e70b99348a5a36802.nq.gz
│   ├── ccba6151b67b3f631d57d900efefd87d4fa35498.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f95e9fc118e9b823d13dcfd6f9cb986471ef083e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 21b84fa1ae64c4616cb681551378688e7d18161d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 22 files
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

[samuelcolvin/pytest-speed](https://github.com/samuelcolvin/pytest-speed)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
