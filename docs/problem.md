# Problem statement

> **Which section is for you:** *In plain terms* is for anyone who's curious. *For contributors* is for developers. *Scratchpad* holds working notes.

## In plain terms

You probably have hundreds of saved passwords, and a lot of them are old, weak, or reused. Fixing them one by one takes forever, so nobody does it. Meanwhile, AI assistants are starting to log into sites for you, and right now that means handing them your password. Keyward fixes both.

## For contributors

### Password debt
Most people have hundreds of saved logins spread across Apple Keychain, one or
more browsers, and maybe a third-party manager like 1Password. Many are weak,
reused, or years old. Some belong to sites that no longer exist. Fixing this by
hand means visiting each site, finding a change-password page, and updating the
vault, so almost nobody does it.

Password managers can *flag* weak or reused passwords, but they can't *act* on
them at scale.

### AI agents need to log in, but shouldn't see passwords
Cloud AI assistants increasingly do real work on the web for people: booking,
buying, managing accounts. That work often needs a login. Today the options are
bad:

- Hand the cloud model the password (it now sits in a remote context, logs, and
  possibly training data).
- Make the human type it every time (defeats the point of an assistant).

### The gap
There is no small, trustworthy, local component whose only job is to handle
credentials: clean them up in bulk, and use them on behalf of a remote agent
without revealing them.

## Scratchpad

_Working notes, half-formed ideas, and to-dos for this topic. These get turned into proper briefs later._

- [ ] Add notes here
