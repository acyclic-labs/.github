# Acyclic Labs

**Building tools that help developers ship faster.** Infrastructure for agent workloads: a harness you compose in Rust, and the filesystem, streams, object storage, machines, and inference underneath it. Forking a workspace, a history, a machine, or a model context shares what hasn't changed instead of copying it.

Two things you can use today:

```sh
npm i -g @acyclic-labs/plugin   # the acyclic plugin: snapshot, fork and rewind your agent's work
```

[`sdk`](https://github.com/acyclic-labs/sdk) — the prerelease Rust SDK and its in-memory reference providers. Registry availability, limits, and prices aren't published yet.

## What we're building

| | |
|---|---|
| **Open-source harness** | Build your agent. Decompose work recursively. Use as much Acyclic infrastructure as you need. |
| **Managed Agent Runtime** | Let Acyclic operate your harness and its selected dependencies. |
| **Filesystem** | Shared workspaces that fork instantly, converge safely, and mount anywhere. |
| **Stream** | One ordered history. Native forks. Durable replay. |
| **Objects** | Fast object storage for the many small artifacts agents create. |
| **Machines** | Elastic, forkable Linux compute without choosing a VM size. |
| **Inference** | Persistent, branchable context for fast, economical agent turns. |

These are contracts being built, not qualified service guarantees — performance, availability, durability, limits, and pricing claims stay inactive until their qualification evidence is published.

Our flagship product, [**Graphcoder**](https://graphcoder.ai), is an AI-powered coding assistant designed to integrate seamlessly into your workflow.

## Who we are

Acyclic Labs, funded by Y Combinator. We build developer tools that prioritize simplicity and speed — [Varun Latthe](mailto:var@acyclic.dev) and [Abhiram Vinjamuri](mailto:ram@acyclic.dev).

Running agent swarms? [Talk to us](https://acyclic.dev).
