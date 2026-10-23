# Installation / 安装说明

Version: **v0.10.26 Public Beta 1 / 公测版 1** (`v0.10.26-beta.1`).

## Requirements / 运行要求

- Windows, Elden Ring, and Shadow of the Erdtree. Development baseline: game **1.17.1**. Other versions are unverified.
- ME3 installed separately. This package contains a ME3 profile; it does not contain `me3.exe` or a ModEngine 2 executable.
- Use the supplied offline profile and back up your saves before testing.

需要 Windows、《艾尔登法环》本体、黄金树幽影 DLC，另行安装 ME3。开发基线为游戏 **1.17.1**，其他版本未验证。包内提供 ME3 配置，不包含 ME3 程序或 ModEngine 2 程序。

## Steps / 安装步骤

1. Download `ELDEN_RING_NIGHTTIDE_v0.10.26_Public_Beta_1.zip` from the release assets. The “Source code” downloads are not the player package.
2. Extract the complete ZIP into a **new directory**. Do not overwrite an old F1/F2/F3/H1/F4 install or add historical patches.
3. Make `me3.exe` available on Windows PATH. The launcher also recognizes the historical `E:\me3\bin\me3.exe` and `E:\me3\me3.exe` locations.
4. Run **`ModEngine/launchmod_eldenring.bat`**. It verifies the runtime files before invoking `nighttide.me3`.
5. If verification reports a missing or changed file, extract the complete package again into a clean directory. If ME3 is not found, correct its installation/PATH; the game has not launched yet.

对应中文步骤：下载完整玩家 ZIP → 完整解压到新目录 → 安装 ME3 并设置 PATH → 运行 **`ModEngine/launchmod_eldenring.bat`**。不要混装旧测试补丁。校验失败时重新完整解压；提示找不到 ME3 时修正 ME3 安装或 PATH。

## Package layout / 文件结构

| Path | Purpose / 用途 |
| --- | --- |
| `ModEngine/launchmod_eldenring.bat` | Single launch entry / 唯一启动入口 |
| `ModEngine/nighttide.me3` | Offline ME3 profile / 离线配置 |
| `ModEngine/verify_files.ps1` | Pre-launch runtime checks / 启动前文件校验 |
| `ModEngine/mod/` | Game mod resources and regulation / 游戏资源与参数 |
| `ModEngine/CaligoHpCapFix.dll` | Existing Caligo HP support module / 已有冰龙 HP 支持模块 |
| `ModEngine/ExpandedTalismanSlots.dll` and `.ini` | Existing extra talisman slot integration / 已有额外护符槽整合 |
| `SHA256_FILES.txt` | Checksums for shipped files / 包内文件校验值 |
| `KNOWN_ISSUES.md` | Unresolved issues and feedback instructions / 未解决问题与反馈说明 |

The runtime checker expects the shipped INI unchanged. Deliberate configuration edits will cause a mismatch; use a separate copy for personal configuration experiments.

启动校验按发布时的原始 INI 检查；自行修改后会报告不一致。需要试改配置时，请另留一份独立副本。

## Feedback / 问题反馈

Report beta version, game version, boss/arena, phase, exact steps, whether the problem survives a reload, and any other installed mods. A short video is useful for grab attachment, hitboxes, critical attacks, and missing sound. Read `KNOWN_ISSUES.md` first.

反馈请包含公测版本、游戏版本、Boss/场地、阶段、操作步骤、重载后是否复现、其他 Mod；动作、判定、处决和声音问题尽量附短视频。先查看 `KNOWN_ISSUES.md`。
