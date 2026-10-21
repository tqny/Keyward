# Keyward (working name)

**A tiny local model that is the only thing allowed to touch your passwords.**

Keyward is an open-source concept for a very small, local language model that
sits between your password managers and everything else, including cloud AI
models. It does two jobs:

1. **Clean up your vault.** Go through saved passwords in bulk, flag weak,
   reused, and stale ones, decide which accounts are worth keeping, and rotate
   the keepers to strong random passwords, saving them back into your password
   manager.
2. **Be the go-between for cloud AI.** When a cloud model is doing a task for
   you and needs to log in somewhere, it asks Keyward over a secure tunnel.
   Keyward fetches the credential locally, fills it in, and reports back. The
   cloud model gets *outcomes, not secrets*.

Keyward is a narrow specialist, not a generalist: fetch this credential, fill
this field, submit this form, report back.

> Status: concept only. No code yet. These docs are meant for collaborators to
> pick up, poke holes in, and build on.

## Docs

- [Problem statement](docs/problem.md)
- [Architecture](docs/architecture.md)
- [Model tiers](docs/model-tiers.md)
- [Password manager integrations](docs/integrations.md)
- [Cloud liaison tunnel](docs/cloud-liaison.md)
- [Use cases](docs/use-cases.md)
- [Security model](docs/security-model.md)
- [Open questions](docs/open-questions.md)

## Principles

- **Local only for secrets.** Plaintext credentials never leave the machine.
- **Small enough for most machines.** Multiple size tiers, from laptops to workstations.
- **Narrow by design.** Limited actions mean a smaller attack surface.
- **User stays in charge.** Deletions and rotations are proposed, then approved.
- **Open source.** Anything that handles your passwords should be auditable.

## License

To be decided (see [open questions](docs/open-questions.md)).
