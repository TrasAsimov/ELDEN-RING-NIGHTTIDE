# NIGHTTIDE Roadmap

## Current public test

**v0.10.38-beta.2 / Public Beta 2** packages the live folder after F8.x iteration. Adel grab lock timing and flat-floor leave/reset are verified in play. Libra amplitude and Heolstor phase-1 hit feel remain open, and that work is paused. Nightreign OST is not shipped. See [known issues](KNOWN_ISSUES.md), [installation](INSTALL.md), and [release history](CHANGELOG.md).

## Immediate priorities

- Dreglord head collision and critical-attack eligibility; corruption gathering, orb effects, and phase-two white artifacts.
- Adel full mouth-follow through the animated grab. Grab lock timing and flat-floor leave/reset (54 m from marker `2054390850`) are already verified.
- Libra, paused at the owner's request: `c7561` bone order still mismatches stock `c7560`. F8.6.2 slide and stub retarget are in the package, and swing amplitude is still wrong. Reach, damage, critical attacks, and summons remain open.
- Heolstor, paused: phase-1 combo still lacks hit feel and SFX. The P1 anibnd overlay is present; the ERR full model is not used. Phase-two cloth, transitions, and victory cleanup remain open.
- Gladius visible activation marker and Rykard post-victory wicker/furnace enemy cleanup.
- Fulghor damage measurements. Dedicated Nightreign boss music is not in this package; `cs_smain.bnk` is the stock bank after the F9 all-boss silence rollback.

## Foundation and balance

- Migrate the historical Ascended-based development branch to a clean independent foundation. **This work remains pending.**
- Preserve only integrations within their applicable permissions and keep upstream attribution current.
- Continue progression, HP/FP/stamina, equipment, talismans, skills, spells, enemy tuning, and reward work with measured game tests.

## Encounters and compatibility

- Validate boss AI, navigation, phases, cameras, lock-on, sound, critical/grab compatibility, rewards, death flags, and save/reload behavior.
- Retain intended enhanced forms where available; Caligo is already enhanced. Insects are excluded from the enhanced-form replacement request.
- Confirm English/Simplified Chinese text and offline ME3 compatibility.
- Maintain one complete player package with a single launch entry; keep development checkpoints and historical tests separate.

A stable release depends on game testing of the unresolved behavior. Archive and parameter checks alone do not establish encounter completion.
