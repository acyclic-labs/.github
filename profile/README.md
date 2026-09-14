# Acyclic Labs

**Building tools that help developers ship faster.** Acyclic is infrastructure for agent workloads: a harness you compose in Rust, and the filesystem, streams, object storage, machines, and inference underneath it. Build a composable agent harness; add the infrastructure your workload needs. One property runs through all of it — forking a workspace, a history, a machine, or a model context shares what hasn't changed instead of copying it.

> **Status.** These pages define the developer contracts being built, not qualified service guarantees. Every product page on [acyclic.dev/docs](https://acyclic.dev/docs) carries its own preview notice, and performance, availability, durability, limits, and pricing claims stay inactive until their qualification evidence is published. Examples are not release announcements.

## What we're building

| | | Status |
|---|---|---|
| [**Open-source harness**](https://acyclic.dev/docs/harness) | Build your agent. Decompose work recursively. Use as much Acyclic infrastructure as you need. | Planned contract |
| [**Managed Agent Runtime**](https://acyclic.dev/docs/managed-agent-runtime) | Let Acyclic operate your harness and its selected dependencies. | Planned contract |
| [**Filesystem**](https://acyclic.dev/docs/filesystem) | Shared workspaces that fork instantly, converge safely, and mount anywhere. | Preview contract |
| [**Stream**](https://acyclic.dev/docs/stream) | One ordered history. Native forks. Durable replay. | Preview contract, not production-qualified |
| [**Objects**](https://acyclic.dev/docs/objects) | Fast object storage for the many small artifacts agents create. | Preview contract, not production-qualified |
| [**Machines**](https://acyclic.dev/docs/machines) | Elastic, forkable Linux compute without choosing a VM size. | Preview contract |
| [**Inference**](https://acyclic.dev/docs/inference) | Persistent, branchable context for fast, economical agent turns. | Intended preview contract |
| [**Agent integrations**](https://acyclic.dev/docs/plugins) | Use Acyclic capabilities from another agent product, or connect it to the harness. | Planned |

What we're building and how the pieces depend on each other: [the roadmap](https://acyclic.dev/docs/roadmap).

Our flagship product, [**Graphcoder**](https://graphcoder.ai), is an AI-powered coding assistant designed to integrate seamlessly into your workflow.

## Public repositories

Most of the stack is private while it is being built and qualified. What is public today:

| | |
|---|---|
| [`sdk`](https://github.com/acyclic-labs/sdk) | The prerelease Rust SDK source and release artifact, with in-memory reference providers. Registry availability, numeric limits, prices, and performance guarantees are not yet published. |
| [`s3s`](https://github.com/acyclic-labs/s3s) | Our fork of the `s3s` S3 service adapter, which the filesystem's hosted crate builds on. |
| [`humaniser`](https://github.com/acyclic-labs/humaniser) | "Human or AI" — a guess-the-author game, built as a research instrument. Separate from the stack above. |

## Who we are

Acyclic Labs, funded by Y Combinator. Acyclic builds developer tools that prioritize simplicity and speed.

- Varun Latthe — var@acyclic.dev
- Abhiram Vinjamuri — ram@acyclic.dev

Running agent swarms? [Talk to us](https://acyclic.dev).
