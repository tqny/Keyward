# Problem statement

## Password debt
Most people have hundreds of saved logins spread across Apple Keychain, one or
more browsers, and maybe a third-party manager like 1Password. Many are weak,
reused, or years old. Some belong to sites that no longer exist. Fixing this by
hand means visiting each site, finding a change-password page, and updating the
vault, so almost nobody does it.

Password managers can *flag* weak or reused passwords, but they can't *act* on
them at scale.

## AI agents need to log in, but shouldn't see passwords
Cloud AI assistants increasingly do real work on the web for people: booking,
buying, managing accounts. That work often needs a login. Today the options are
bad:

- Hand the cloud model the password (it now sits in a remote context, logs, and
  possibly training data).
- Make the human type it every time (defeats the point of an assistant).

## The gap
There is no small, trustworthy, local component whose only job is to handle
credentials: clean them up in bulk, and use them on behalf of a remote agent
without revealing them.
