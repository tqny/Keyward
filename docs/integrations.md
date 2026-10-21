# Password manager integrations

> **Which section is for you:** *In plain terms* is for anyone who's curious. *For contributors* is for developers. *Scratchpad* holds working notes.

## In plain terms

Keep using the password manager you already have, whether that's Apple Passwords, Chrome, Firefox, or 1Password. Keyward works with it and saves new passwords right back into it.

## For contributors

Keyward should work with the managers people already use, rather than becoming
another one.

| Manager | Read | Write back | Notes |
|---|---|---|---|
| Apple Keychain / Passwords | Likely via system APIs | Likely | macOS / iOS permission prompts apply |
| Chrome / Chromium browsers | Export or local store | Harder | Encrypted with OS keys; may need extension |
| Firefox | Local store | Possible | Primary password support needed |
| Safari | Via Keychain | Via Keychain | |
| 1Password | CLI / SDK / Connect | Yes | Good official tooling |
| Bitwarden | CLI / API | Yes | Open source, natural ally |
| Others (Dashlane, LastPass, KeePass) | Varies | Varies | Community adapters |

All of the above is unverified and needs research per platform.

### Adapter contract (sketch)
- `list()` — entries with metadata (site, username, last changed), not plaintext
- `get(handle)` — returns the secret only to the fill pipeline, never to the model
- `update(handle, new_secret)` — writes a rotated password back
- `delete(handle)` — only after explicit user approval

### Write-back safety
Rotation must never lose a password. Save the new password (or a pending copy)
in the manager *before* submitting the change on the site, then confirm.

## Scratchpad

_Working notes, half-formed ideas, and to-dos for this topic. These get turned into proper briefs later._

- [ ] Add notes here
