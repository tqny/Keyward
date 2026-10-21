# Use cases

## 1. Bulk rotation of old, reused passwords
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

## 2. Cloud-model-driven logins without exposing secrets
A cloud assistant is booking a trip and needs the user's airline login. It asks
Keyward to log in. Keyward fills the credential locally and replies
`logged_in`. The assistant continues the task without ever having seen the
password.

## Other possibilities
- Breach response: rotate every account touched by a known breach.
- Scheduled hygiene: rotate high-value accounts every N months.
- Migration: consolidate logins from several managers into one.
