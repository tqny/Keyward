# Cloud liaison tunnel

> **Which section is for you:** *In plain terms* is for anyone who's curious. *For contributors* is for developers. *Scratchpad* holds working notes.

## In plain terms

When your AI assistant needs to log in somewhere, it asks Keyward. Keyward logs in on your computer and tells the assistant whether it worked. The assistant never sees your password.

## For contributors

Lets a cloud model provider use your logins without ever seeing them.

### Flow
1. A cloud model, working on your behalf, reaches a login page.
2. It sends Keyward a request: "Log in to `example.com` as the user's main
   account" (plus page context or a browser session reference).
3. Keyward checks policy: is this domain allowed, is this provider allowed, does
   this need user approval?
4. Keyward fetches the credential locally and fills and submits the form.
5. Keyward reports back an outcome: `logged_in`, `failed: wrong password`,
   `needs_2fa`, `needs_user`, and so on. Never the secret.

### Request vocabulary (sketch)
Keep it small on purpose:
- `login(site, account)`
- `fill(field, credential_ref)`
- `submit(form)`
- `status()`

No `get_password`. There is no verb that returns plaintext.

### Tunnel properties
- Mutually authenticated, end-to-end encrypted.
- Paired per provider by the user, revocable at any time.
- Works across machines: whichever machine holds the vault runs Keyward.
- Every request logged locally.

### Where the browser runs
Open design question. If the browser runs in the cloud, the secret must be
typed into a remote session, which means it does leave the machine. The cleaner
option is that the authenticated browser session runs locally, or that only a
session token (not the password) is handed over. See
[open questions](open-questions.md).

## Scratchpad

_Working notes, half-formed ideas, and to-dos for this topic. These get turned into proper briefs later._

- [ ] Add notes here
