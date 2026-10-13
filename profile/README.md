# Acyclic Labs

**Rapid agent swarms. Make any agentic workflow exponentially faster.**

Acyclic Labs builds rapid agent swarms. Hand a task to a swarm and it fans the work out across many agents, each in its own sandbox, then merges what they produce, so long agentic workflows finish exponentially faster.

Two things you can use today:

[**Managed Agents**](https://acyclic.dev/agents): one command hands a task to a swarm of agents working in parallel.

```sh
npm install -g @acyclic-labs/cli
acyclic swarm login
acyclic swarm run --task "fix the flaky test in tests/api" --dir . --watch
```

[**sdk**](https://github.com/acyclic-labs/sdk): prefer to self-host? The harness is open source and works without managed hosting.

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

Acyclic Labs, funded by Y Combinator. We build developer tools that prioritize simplicity and speed — [Varun Latthe](mailto:var@acyclic.dev) and [Abhiram Vinjamuri](mailto:ram@acyclic.dev).

Running agent swarms? [Talk to us](https://acyclic.dev).
