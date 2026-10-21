# Use cases

> **Which section is for you:** *In plain terms* is for anyone who's curious. *For contributors* is for developers. *Scratchpad* holds working notes.

## In plain terms

Clean up years of bad passwords in one go, and let AI assistants log in for you without handing over your passwords.

## For contributors

### 1. Bulk rotation of old, reused passwords
1. Keyward reads all vault entries (metadata first).
2. It flags weak, reused, and old passwords.
3. For each account it decides: **keep**, **likely trash**, or **can't rotate**.
   - Site gone or domain parked: report it, suggest deleting.
   - No change-password flow found: report it, user decides.
   - Account clearly unused or low value: suggest deleting.
4. User reviews and approves the plan.
5. For keepers, Keyward logs in, changes the password to a strong random one,
   saves it back to the password manager, and verifies the new one works.
6. A final report lists what was rotated, deleted, skipped, and why.

### 2. Cloud-model-driven logins without exposing secrets
A cloud assistant is booking a trip and needs the user's airline login. It asks
Keyward to log in. Keyward fills the credential locally and replies
`logged_in`. The assistant continues the task without ever having seen the
password.

### Other possibilities
- Breach response: rotate every account touched by a known breach.
- Scheduled hygiene: rotate high-value accounts every N months.
- Migration: consolidate logins from several managers into one.

## Scratchpad

_Working notes, half-formed ideas, and to-dos for this topic. These get turned into proper briefs later._

- [ ] Add notes here
