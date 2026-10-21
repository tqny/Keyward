# Security model

## What we protect
Plaintext credentials, and the ability to use them.

## Threats to think through
- **Prompt injection from web pages.** A malicious page tells the model to type
  a password into the wrong field or site. Mitigation: domain binding enforced
  by the policy engine, not the model.
- **A compromised or misbehaving cloud model.** Mitigation: no plaintext verbs,
  per-domain allowlists, approval for sensitive actions, rate limits.
- **Malware on the local machine.** Largely out of scope, same as any password
  manager, but Keyward should not make it worse.
- **Lost passwords during rotation.** Mitigation: write-back before submit,
  verify after.
- **Model leaking secrets in output.** Mitigation: the model handles references,
  not plaintext.

## Guarantees we want
- Plaintext never crosses the tunnel.
- Every access is logged locally.
- Destructive actions (delete, bulk rotate) require user approval.
