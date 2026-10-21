# Keyward (working name)

**A tiny local model that is the only thing allowed to touch your passwords.**

> **Which section is for you:** *Why you'd want this* is for anyone who's curious. *For contributors* is for developers. *Scratchpad* holds working notes. Every doc in `docs/` uses the same three sections.

## Why you'd want this

- **Fix years of bad passwords in one go.** Keyward checks every password saved in Apple Passwords/Keychain, your browsers, and 1Password. It finds the weak, reused, and old ones, and spots accounts you don't need anymore (including sites that no longer exist). Then it changes the ones you keep to strong new passwords and saves them back for you.
- **Let AI log in for you without giving it your password.** When a cloud AI assistant needs to sign in somewhere, Keyward does the login on your computer and just tells the assistant it worked.
- **Your passwords stay on your machine.** It's small, it runs locally, and it's open source, so anyone can check what it does.

## For contributors

Keyward is a very small local language model, in several size tiers, wrapped in a deterministic policy engine. It connects to password managers through adapters and drives a local browser to fill forms. It talks to cloud model providers over an encrypted tunnel that carries requests and outcomes only, never plaintext. The model is a narrow specialist: fetch this credential, fill this field, submit this form, report back.

> Status: concept only. No code yet.

Places to plug in:
- Base model, fine-tuning, and tier benchmarks: [model tiers](docs/model-tiers.md)
- Password manager adapters: [integrations](docs/integrations.md)
- Tunnel protocol and request vocabulary: [cloud liaison](docs/cloud-liaison.md)
- Policy engine and threat model: [architecture](docs/architecture.md), [security model](docs/security-model.md)

### Docs
- [Problem statement](docs/problem.md)
- [Architecture](docs/architecture.md)
- [Model tiers](docs/model-tiers.md)
- [Password manager integrations](docs/integrations.md)
- [Cloud liaison tunnel](docs/cloud-liaison.md)
- [Use cases](docs/use-cases.md)
- [Security model](docs/security-model.md)
- [Open questions](docs/open-questions.md)

### Principles

- **Local only for secrets.** Plaintext credentials never leave the machine.
- **Small enough for most machines.** Multiple size tiers, from laptops to workstations.
- **Narrow by design.** Limited actions mean a smaller attack surface.
- **User stays in charge.** Deletions and rotations are proposed, then approved.
- **Open source.** Anything that handles your passwords should be auditable.

### License

To be decided (see [open questions](docs/open-questions.md)).

## Scratchpad

_Running notes for tracking the idea until there's time for proper briefs._

- [ ] Pick a real name
- [ ] Turn use cases into briefs
- [ ] Decide when to publish publicly
