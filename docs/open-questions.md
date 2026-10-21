# Open questions

> **Which section is for you:** *In plain terms* is for anyone who's curious. *For contributors* is for developers. *Scratchpad* holds working notes.

## In plain terms

Keyward is an early idea. These are the big things still to figure out, and good places to jump in if you want to help.

## For contributors

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

## Scratchpad

_Working notes, half-formed ideas, and to-dos for this topic. These get turned into proper briefs later._

- [ ] Add notes here
