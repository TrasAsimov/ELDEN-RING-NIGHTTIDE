# ELDEN RING: NIGHTTIDE

### 艾尔登法环：黑夜入侵

[简体中文](README.zh-CN.md) · [Installation](INSTALL.md) · [Known issues](KNOWN_ISSUES.md) · [Changelog](CHANGELOG.md) · [Credits](CREDITS.md)

NIGHTTIDE is an experimental Elden Ring overhaul with progression and balance changes, reworked encounters, and selected Nightreign boss integrations.

**Current build: v0.10.38 Public Beta 2 (`v0.10.38-beta.2`).** Download the complete player ZIP `ELDEN_RING_NIGHTTIDE_v0.10.38_Public_Beta_2.zip` from [GitHub Releases](https://github.com/TrasAsimov/ELDEN-RING-NIGHTTIDE/releases). GitHub's automatically generated “Source code” archives contain documentation, not the playable mod.

This beta packages the live folder after F8.x iteration. Adel grab lock timing and flat-floor leave/reset (F8.4 / F8.4.1) were verified in play; the leave zone is 54 m from marker `2054390850`. Libra's swing amplitude and Heolstor's phase-1 hit feel/SFX are still wrong, and that work is paused. An F9 `cs_smain.bnk` experiment that silenced all boss music was rolled back to the stock bank; Nightreign OST is not shipped. Read [the issue list](KNOWN_ISSUES.md) before installing.

## Install

Use Elden Ring with Shadow of the Erdtree and a separately installed ME3. The development baseline targets game version 1.17.1; compatibility with other versions has not been verified. Extract the entire ZIP into a new folder, then run `ModEngine/launchmod_eldenring.bat`. Do not layer Public Beta 1 or older tests over this package. See [INSTALL.md](INSTALL.md) for details.

The supplied profile starts offline. Back up saves before testing an overhaul. Play checks this cycle cover the Adel grab-lock and flat-floor leave behavior named above. They do not certify Libra, Heolstor, music replacement, or the other open encounters.

## Project status

The project grew from an Ascended-based development branch. This beta retains that historical basis plus subsequent NIGHTTIDE integrations; the planned migration to a clean independent foundation is still pending. It is not an official continuation of Ascended and is not affiliated with FromSoftware, Bandai Namco, or third-party mod authors.

NIGHTTIDE is a non-commercial fan project. Attribution is recorded in [CREDITS.md](CREDITS.md); inclusion does not transfer ownership of game or third-party assets.

Report the version, arena, boss phase, reproduction steps, and a short video where possible in [Issues](https://github.com/TrasAsimov/ELDEN-RING-NIGHTTIDE/issues). Please distinguish repeatable problems from one-time observations.
