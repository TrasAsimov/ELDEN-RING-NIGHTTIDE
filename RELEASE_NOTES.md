## 艾尔登法环：黑夜入侵 v0.10.38 公测版 2

以现行公测目录在 F8.x 内测之后整理的完整玩家包。请完整解压到新目录，不要叠加公测版 1 或更早的测试补丁。

### 本轮确认

- **大嘴 Adel**：抓取锁定时机与平地离场/重置（F8.4 / F8.4.1）已实机验证。离场区为标记 `2054390850` 外 54 m。全程跟随动画嘴部仍是未验收的 F4 候选，本次确认不包含该项。
- **Boss BGM**：F9 对 `cs_smain.bnk` 的试验曾使全部 Boss 音乐无声，已回滚至原版 bank（1390900 字节，SHA-256 前缀 `ca3d50f2eadebd0c`）。**未附带**黑夜君临 OST，Boss 音乐不能视为已修复。

### 仍未解决（工作已暂停）

- **山羊 Libra**：自定义 `c7561` 与原版 `c7560` 骨骼顺序不一致。F8.6.2 骨骼滑动 + stub 重定向仍在包内，挥击幅度仍然错误。已按所有者要求暂停。攻击范围、伤害、处决和召唤与公测版 1 相同。公测版 1 关于 H1 靠近崩溃回退的说明保持不变，本轮没有新的靠近结果。
- **不得其名 Heolstor**：一阶段连招仍无打击感 / 音效。P1 anibnd 覆盖层仍在；未使用 ERR 完整模型。工作已暂停。二阶段斗篷、阶段切换、战后血条和雾门清理与公测版 1 相同，仍未验收。
- 其余 F4 继承候选（垃圾王处决、三狼入口亮光、拉卡德柳条人、人马伤害等）与公测版 1 相同。

### 打包

玩家 ZIP：**ELDEN_RING_NIGHTTIDE_v0.10.38_Public_Beta_2.zip**（由发布者另行上传到本 Release 的 Assets）。包内只有 `ModEngine/` 和玩家文档。不含 `_pre_*`、`_nightreign_chr_stash`、`_f8_crash_stash`、内部 `TEST_NOTES`，也不含已弃用的 F9 wem `sd/wem/91|92|93`。

仓库 `SHA256SUMS.txt` 仍只有公测版 1 归档的 SHA-256。本 ZIP 的归档校验值请写在资产上传之后；下表是包内关键文件的大小和 SHA-256 **前缀**，不是完整摘要。

| File | Bytes | SHA-256 prefix | Note |
| --- | --- | --- | --- |
| `regulation.bin` | 3067232 | `a067a4b2e02cd26f` | |
| `common.emevd.dcx` | 108762 | `3b322c653e62e71c` | |
| `c0000.anibnd.dcx` | 14932200 | `b571478cc3dc60b2` | |
| `c7561.chrbnd.dcx` | 25690988 | `bd7102122a656736` | |
| `c7561.anibnd.dcx` | 17968 | `537c2e98635e548f` | stub |
| `c7580.anibnd.dcx` | 2757156 | `409c50ebbea207fe` | |
| `cs_smain.bnk` | 1390900 | `ca3d50f2eadebd0c` | stock, post-rollback |

### 下载与安装

从 Assets 下载 **ELDEN_RING_NIGHTTIDE_v0.10.38_Public_Beta_2.zip**，完整解压到新目录。需要本体、黄金树幽影 DLC 和另行安装的 ME3，开发基线为游戏 1.17.1。运行 `ModEngine/launchmod_eldenring.bat`，配置默认离线。不要下载自动生成的 Source code 作为游戏安装包。

1. 备份存档，确认本体和黄金树幽影 DLC 能正常启动。
2. 下载完整玩家 ZIP，完整解压到全新目录，不覆盖公测版 1 或旧测试包。
3. 从 [ME3 官方发布页](https://github.com/garyttierney/me3/releases/latest) 下载并运行 `me3_installer.exe`，按向导安装。
4. 运行解压后的 `ModEngine/launchmod_eldenring.bat`；校验通过后由 ME3 离线启动。
5. 提示 ME3 not found、Missing file 或 File mismatch 时，查看 [安装说明](https://github.com/TrasAsimov/ELDEN-RING-NIGHTTIDE/blob/main/INSTALL.md)。

[安装说明](https://github.com/TrasAsimov/ELDEN-RING-NIGHTTIDE/blob/main/INSTALL.md) · [更新日志](https://github.com/TrasAsimov/ELDEN-RING-NIGHTTIDE/blob/main/CHANGELOG.md) · [已知问题](https://github.com/TrasAsimov/ELDEN-RING-NIGHTTIDE/blob/main/KNOWN_ISSUES.md) · [致谢与来源](https://github.com/TrasAsimov/ELDEN-RING-NIGHTTIDE/blob/main/CREDITS.md)

本版为公测预发布。实机确认仅覆盖大嘴抓取锁定时机与平地离场重置。山羊幅度、不得其名一阶段打击感和黑夜君临专属音乐均未修好。测试前请备份存档。

**English:** Public Beta 2 player package from the live folder after F8.x. Adel grab lock timing and flat-floor leave/reset (F8.4 / F8.4.1) verified in play; leave zone is 54 m from marker `2054390850`. Libra `c7561` vs `c7560` bone order still mismatches and swing amplitude is still wrong (F8.6.2 slide + stub remain; work paused). The Beta 1 H1 proximity-crash rollback note is unchanged. Heolstor phase-1 combo still has no hit feel/SFX (P1 anibnd overlay present; ERR full model not used; work paused). F9 `cs_smain.bnk` experiment silenced all boss music and was rolled back to the stock bank (`ca3d50f2eadebd0c`, 1390900 bytes). Nightreign OST is not shipped. Other F4 candidates are unchanged from Beta 1. ZIP is `ELDEN_RING_NIGHTTIDE_v0.10.38_Public_Beta_2.zip` (`ModEngine/` + player docs only).
