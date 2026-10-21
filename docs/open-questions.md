# Open questions

- **Name.** "Keyward" is a placeholder.
- **Base model.** Which small open model to start from, and how to fine-tune it
  on login and change-password flows?
- **Tier sizes.** What hardware targets and what success rate counts as
  "acceptable" per tier?
- **Browser location.** For the cloud liaison, does the browser run locally, or
  do we hand over session tokens? How do we avoid the secret ever being typed
  into a remote session?
- **2FA.** How to handle SMS, authenticator codes, and passkeys during rotation
  and logins?
- **Passkeys.** Do they make part of this obsolete, and should Keyward help
  migrate accounts to passkeys?
- **Platform access.** What do Apple, Google, and browser vendors actually allow
  for programmatic read and write of saved passwords?
- **Site terms.** How to handle sites that block automation or bots?
- **Protocol.** Should the liaison tunnel use an existing standard (for example
  MCP) or a new minimal protocol?
- **License.** Apache-2.0, MIT, or something copyleft?
- **Trust and audits.** How to earn trust for software that touches every
  password: reproducible builds, third-party audits?
