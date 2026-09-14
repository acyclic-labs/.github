# Acyclic Labs

**Infrastructure for agents that fork.** Coding agents are cheap to run and expensive to trust: they write to your working tree, and the only way to try five approaches is to run five copies of everything. We build the substrate underneath — a filesystem, a stream log, an object store, and elastic machines that all share one property: forking a workspace, a history, or a running machine is a cheap operation, not a copy.

> Status, stated once: the [plugin](https://acyclic.dev/docs/plugins) is built and shipping (four of five launches, published to npm, macOS and Linux). Everything else on this page is under active implementation and **not production-qualified** — the docs pages define the intended contract and carry their own preview notices. Performance, availability, and durability claims stay inactive until the qualification evidence is published. We would rather you read that here than discover it in a benchmark.

## The stack

| Piece | What it does | Status | Docs |
|---|---|---|---|
| **Graphcoder** | Multi-agent coding runtime: web, desktop, and CLI shells over a shared daemon and inference/hypervisor services. The product the stack below exists to serve. | In development, [graphcoder.ai](https://graphcoder.ai) | — |
| **Plugin** (`acyclic`) | Local agent-native state engine: Merkle snapshot store, turn-linked timeline, copy-on-write forks, safe mode. Delivered as adapters for Claude Code, Codex, Cursor, Claude Desktop, VS Code — anything that runs a shell command or speaks MCP. | Launches 1–4 built, on npm as `@acyclic-labs/plugin`; Launch 5 (monorepo index) is spec | [docs](https://acyclic.dev/docs/plugins) |
| **Filesystem** | Fork, join, and mount shared agent workspaces through Rust, a native filesystem, or S3. | Preview contract | [docs](https://acyclic.dev/docs/filesystem) |
| **Stream** | Fork exact ordered histories, append with tail CAS, replay durably without S3 on the hot path. | Preview contract, not production-qualified | [docs](https://acyclic.dev/docs/stream) |
| **Objects** | Large populations of small artifacts, immutable versions, instant isolated snapshots. | Preview contract, not production-qualified | [docs](https://acyclic.dev/docs/objects) |
| **Machines** | Elastic Linux machines that expand from idle to peak without picking a CPU/RAM shape, and fork from a checkpoint. | Preview contract | [docs](https://acyclic.dev/docs/machines) |
| **Inference** | Persistent, branchable agent context with explicit edits, model transfer, work-based billing. | Intended preview contract | [docs](https://acyclic.dev/docs/inference) |
| **Harness** | Compose models, tools, and agent behavior in Rust; recursive fork-join workflows over local, third-party, or Acyclic providers. | Planned contract | [docs](https://acyclic.dev/docs/harness) |
| **Managed Agent Runtime** | The same harness, hosted, with explicit capacity, recovery, and organization controls. | Planned contract | [docs](https://acyclic.dev/docs/managed-agent-runtime) |

How the pieces depend on each other, and what lands in what order: [the roadmap graph](https://acyclic.dev/docs/roadmap).

## Repositories

Most of the stack is private while it is being qualified. What is public:

| Repo | What it is |
|---|---|
| [`sdk`](https://github.com/acyclic-labs/sdk) | The Acyclic SDK and in-memory reference providers — the contract, runnable without an account. |
| [`humaniser`](https://github.com/acyclic-labs/humaniser) | "Human or AI" — a guess-the-author game, built as a research instrument. Unrelated to the stack above. |
| [`s3s`](https://github.com/acyclic-labs/s3s) | Our fork of the `s3s` S3 service adapter; the filesystem's hosted crate builds on it. |

The plugin, filesystem, stream, objects, machines, inference, and harness repos are private today. The plugin is Apache-2.0 and its releases already ship SLSA build provenance, per-binary SBOM attestations, and a `SHA256SUMS` the installer verifies — the binary you install from npm is checkable without the source being open yet.

## Who we are

Acyclic Labs, backed by Y Combinator. Two founders:

- Varun Latthe — var@acyclic.dev
- Abhiram Vinjamuri — ram@acyclic.dev

Running agent swarms and hitting the substrate underneath? [acyclic.dev](https://acyclic.dev) — or mail either of us directly.
