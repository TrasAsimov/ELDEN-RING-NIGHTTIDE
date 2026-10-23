# Changelog / 更新日志

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
