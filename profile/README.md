# Acyclic Labs

**Rapid agent swarms. Make any agentic workflow exponentially faster.** Underneath the swarms is infrastructure for agent workloads: a harness you compose in Rust, and the filesystem, streams, object storage, machines, and inference underneath it. Forking a workspace, a history, a machine, or a model context shares what hasn't changed instead of copying it.

Things you can use today:

```sh
npm i -g @acyclic-labs/cli      # the acyclic CLI: dispatch a swarm, watch it, pull the result into your repo
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

## Who we are

Acyclic Labs, backed by Y Combinator — [Varun Latthe](mailto:var@acyclic.dev) and [Abhiram Vinjamuri](mailto:ram@acyclic.dev).

Start a swarm at [acyclic.dev](https://acyclic.dev), or [talk to us](mailto:ram@acyclic.dev).
