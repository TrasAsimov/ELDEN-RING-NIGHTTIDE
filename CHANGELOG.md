# Changelog / 更新日志

## v0.10.38-beta.2 — Public Beta 2 / 公测版 2

Release date: **2026-11-06**.

Built from the live Public Beta folder after F8.x internal iteration. Obsolete `_pre_*` / stash directories and unused F9 Nightreign BGM wems are stripped from the player ZIP.

### Confirmed this cycle / 本轮确认

- **Adel (大嘴)**: grab lock timing and flat-floor leave/reset (F8.4 / F8.4.1) verified in play. Arena leave uses a 54 m zone from marker `2054390850`.
- **Boss BGM bank**: F9 `cs_smain.bnk` experiment silenced all boss music and was rolled back to the stock bank (SHA-256 prefix `ca3d50f2`, 1390900 bytes). Nightreign OST wiring is **not** shipped.

### Still broken / 仍未解决（已知）

- **Libra (山羊)**: custom `c7561` skeleton bone-order mismatch vs stock `c7560`. F8.6.2 bone-slide + stub retarget remains on disk; swing amplitude still wrong in play. Work paused at the owner's request.
- **Heolstor (不得其名)**: Phase-1 combo still lacks hit feel / SFX. P1 anibnd overlay remains; ERR full model path not used. Work paused.
- Other inherited F4 candidates (Rykard wicker cleanup, Gladius lights, Adel full mouth-follow, Dreglord critical, Fulghor damage, and the rest of the Beta 1 list) are unchanged from Public Beta 1.

### Package hygiene / 打包清理

- Player ZIP: `ELDEN_RING_NIGHTTIDE_v0.10.38_Public_Beta_2.zip`. It contains only `ModEngine/` plus player docs. No `_pre_*`, `_nightreign_chr_stash`, `_f8_crash_stash`, or internal `TEST_NOTES`.
- Orphan `sd/wem/91|92|93` Nightreign tracks removed (bank never shipped).

### Live file markers / 在线文件标记

Sizes and SHA-256 prefixes from the live package. These are prefixes, not full digests. The player ZIP archive checksum is published with the GitHub Release asset.

| File | Bytes | SHA-256 prefix | Note |
| --- | --- | --- | --- |
| `regulation.bin` | 3067232 | `a067a4b2e02cd26f` | |
| `common.emevd.dcx` | 108762 | `3b322c653e62e71c` | |
| `c0000.anibnd.dcx` | 14932200 | `b571478cc3dc60b2` | |
| `c7561.chrbnd.dcx` | 25690988 | `bd7102122a656736` | |
| `c7561.anibnd.dcx` | 17968 | `537c2e98635e548f` | stub |
| `c7580.anibnd.dcx` | 2757156 | `409c50ebbea207fe` | |
| `cs_smain.bnk` | 1390900 | `ca3d50f2eadebd0c` | stock, post-rollback |

中文：本版为大嘴抓取锁定时机与平地离场重置已实测通过的整合公测包；山羊幅度与不得其名一阶段打击感仍未修好并已暂停；F9 改 bank 曾导致全 BOSS 无音乐，已回滚原版 bank，未附 Nightreign OST。发布 ZIP 已剔除全部备份目录与无用 wem。

## v0.10.26-beta.1 — Public Beta 1 / 公测版 1

Release date: **2026-10-23**.

- Consolidated the F4 development state into one complete player ZIP. No old patches need to be layered onto this release.
- Removed historical `Four_Nightlords_T1` and `Gladius_T1` audit directories and superseded test/update reports from the player package.
- Replaced the version-specific H1 launcher/profile/checker names with `launchmod_eldenring.bat`, `nighttide.me3`, and `verify_files.ps1`; kept one launch entry and the existing offline behavior.
- Replaced duplicate/incremental attribution with a consolidated credits file. Preserved all credited contributors from the baseline.
- Added bilingual installation instructions, current known issues, and fresh file/archive SHA-256 checksums.
- Preserved F4 gameplay candidates and the H1 Libra rollback. **No new gameplay, model, grab, critical, music, or damage fix is introduced by this packaging release.**

中文：以 F4 为基线发布单一完整公测 ZIP；移除历史开发审计目录和过期测试说明；统一启动入口、ME3 配置和校验脚本名称；合并重复署名；补齐安装说明、已知问题和新校验值。保留 F4 候选及 H1 山羊回退。**本次仅整理发布，没有新增战斗修复。**

### Inherited development candidates / 继承的开发候选

- Adel: follow mode adjusted alongside the animated mouth attachment; full mouth-follow behavior remains unverified.
- Rykard: post-victory-only removal candidate for the wicker/furnace enemy; the enemy remains during Rykard's fight.
- Gladius: activation effect attachment aligned with the Dreglord setup; visibility still needs game verification.
- Heolstor: four malformed private material strings corrected; simplified opaque materials still differ from the intended cloth appearance. Two missing sound ID types replaced across nine animations with existing same-boss alternatives.
- Libra: H1 rollback retained after a reported F3 proximity crash; the underlying combat and summon problems remain.

中文：继承大嘴抓取跟随组合、拉卡德胜利后柳条人清理、三狼入口光效挂点、不得其名四份材质字符串及九段动作中的两类缺失音效替代。上述候选均不能视为已通过完整实机验收。

### Validation / 验证范围

The F4 source reconstruction and static verification are recorded in the development repository. This public package is checked for archive CRC, every shipped member's checksum, runtime preservation, one launch entry, and configuration references. These checks do not validate the Windows renderer, audio output, animation playback, collision, boss AI, or encounter completion.

F4 重建和静态检查记录保存在开发仓库。公测包检查 ZIP CRC、所有包内文件哈希、运行资源保留、唯一启动入口及配置引用；没有验证 Windows 渲染、声音播放、动作碰撞、Boss AI 或整场战斗。
