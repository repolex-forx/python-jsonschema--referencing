# Repolex Knowledge Graph of python-jsonschema/referencing

RDF knowledge graph data for [python-jsonschema/referencing](https://github.com/python-jsonschema/referencing), parsed by [repolex](https://repolex.ai).

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
rlex download python-jsonschema/referencing
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 40be109b70dddced5bd1c1ee44c1a71301c120cd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 40be109b70dddced5bd1c1ee44c1a71301c120cd
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e73ef10d6e3256c30227b544e69bbfa9d3e5168.nq.gz
│   ├── 15ba57bed85cdb638e7f77beaa868810e47bb497.nq.gz
│   ├── 22876b1699989d1c4cccea0e7b1cd856052b460d.nq.gz
│   ├── 2ada3ec2f1b0c6139698677faadd767b52941175.nq.gz
│   ├── 2fab5983995e128fac32b63cdc0569762f771526.nq.gz
│   ├── 3267fc70732e73c0a888d9f60551ad9373ed6d16.nq.gz
│   ├── 3a83c211972b5f6ba3f3d5c1afce7b756b4b7838.nq.gz
│   ├── 3edddbc3d96581e1c74069baa873900495366bab.nq.gz
│   ├── 4b8ae9177c197456bb3bbd62d4c1875bc95ff28b.nq.gz
│   ├── 68ede2dd58eff136aa581ff93fbb15804e8f63f7.nq.gz
│   ├── 6ab32d6c2f0126cb78446bea62cba78a6bf9d420.nq.gz
│   ├── 6d16afda26c78daab25ed26f9a27eed1b75e0c09.nq.gz
│   ├── 72abd6da33102621f24ad3e8c501dade86d525c2.nq.gz
│   ├── 731e35dbb18f2466bc0843fd5d81b2249e9c769a.nq.gz
│   ├── 7ed5ab60720471dac067b544b877a4a3960ad3a6.nq.gz
│   ├── 920aad97af3b94ef6a810a30279cc8d32750210f.nq.gz
│   ├── 938fe0e83a96a0c00217b0084c0d983845f0b8e0.nq.gz
│   ├── 93cedcd122487421101d9bff69700604bae9b36b.nq.gz
│   ├── 93e77a78717183c3290427a448993e0bb997cfe4.nq.gz
│   ├── 9d1e0987bfc323000b570d680343f00c53ddbc3d.nq.gz
│   ├── a0e9648d3291635ca9b401118fda0cee224dd136.nq.gz
│   ├── a53d093149b8b9200400af37edfbee6a35ca25f7.nq.gz
│   ├── a78fa9fb156bcb0e478ef45f84d84a396d5cfa6a.nq.gz
│   ├── a9f853e43069b8e3f8a156a4af2b1198a004230d.nq.gz
│   ├── ae85b865fed622afe83e8d6b7b17a1f0d174aba3.nq.gz
│   ├── c80714d0132bebbec33401f42a2e06aee3fed9c6.nq.gz
│   ├── d0a8f8ad9975d1a760bca14dea7b60d41fb8ea75.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── db926a20b361f2b140579284e9aefcfc9daaabce.nq.gz
│   ├── de5ccfa1e87f4d3ada3320fc940de16432580311.nq.gz
│   ├── e09207d7e4b90aba221181d87886fd4f54038abf.nq.gz
│   ├── e162d1621bbd125a6d36f99b137b42bb166b9df6.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eca6db2bc88efb8c0183f260e8a34af6701ffbd2.nq.gz
│   ├── ecd1ed342b198b70e7fb311fe1ae57e867eb6a2c.nq.gz
│   ├── f4132658093e110d03243411105a529875e17cfc.nq.gz
│   ├── f8a9afb4d181c6f4788ae9210093ee2932d83d4f.nq.gz
│   ├── fbe127e51aaf3db89c92cf782023dc070347af07.nq.gz
│   └── fd4a0d1df0186f44e4b993310bb6a2613cfa9775.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 40be109b70dddced5bd1c1ee44c1a71301c120cd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[python-jsonschema/referencing](https://github.com/python-jsonschema/referencing)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
