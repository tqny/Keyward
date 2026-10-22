# Security model

> **Which section is for you:** *In plain terms* is for anyone who's curious. *For contributors* is for developers. *Scratchpad* holds working notes.

## In plain terms

Your passwords never leave your computer. Nothing gets deleted or changed without your OK, and you get a record of every time a password was used.

## For contributors

### What we protect
Plaintext credentials, and the ability to use them.

### Threats to think through
- **Prompt injection from web pages.** A malicious page tells the model to type
  a password into the wrong field or site. Mitigation: domain binding enforced
  by the policy engine, not the model.
- **A compromised or misbehaving cloud model.** Mitigation: no plaintext verbs,
  per-domain allowlists, approval for sensitive actions, rate limits.
- **Cloud request escalating to arbitrary root.** A cloud model (compromised,
  misled, or buggy) uses a sudo request to run something other than what was
  vetted, such as extra arguments, chained commands, or a script that changes
  between approval and run. Mitigation: exact-command allowlist matching in the
  policy engine (not the model), no shell expansion, phone approval for
  anything off the list, and every privileged run logged.
- **Malware on the local machine.** Largely out of scope, same as any password
  manager, but Keyward should not make it worse.
- **Lost passwords during rotation.** Mitigation: write-back before submit,
  verify after.
- **Model leaking secrets in output.** Mitigation: the model handles references,
  not plaintext.

### Guarantees we want
- Plaintext never crosses the tunnel.
- Every access is logged locally.
- Destructive actions (delete, bulk rotate) require user approval.

## Scratchpad

_Working notes, half-formed ideas, and to-dos for this topic. These get turned into proper briefs later._

- [ ] Add notes here
