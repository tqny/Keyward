# Model tiers

Keyward should run on most machines, so it ships in several sizes. Each tier
trades capability for footprint.

| Tier | Rough target | What it should handle |
|---|---|---|
| Tiny | Runs on CPU on older laptops | Standard login forms, vault audits (weak / reused / age), simple fills |
| Small | Modern laptop, light GPU or Apple Silicon | Multi-step logins, most change-password flows, judging dead or junk sites |
| Medium | Workstation or strong GPU | Unusual flows, messy page layouts, recovering from errors mid-rotation |

Sizes and hardware targets are placeholders to be set once benchmarking starts.

## Notes
- Vault auditing (strength, reuse, age) is mostly deterministic and needs little
  or no model.
- The hard part is understanding arbitrary websites, which is where bigger tiers
  earn their keep.
- A tier could fall back to asking the user when it isn't confident, rather than
  guessing.
- "Acceptability" per tier should be measured: a public benchmark of real
  login and change-password flows would help.
