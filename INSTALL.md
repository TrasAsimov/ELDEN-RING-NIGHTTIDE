# Installation / 安装说明

Version: **v0.10.26 Public Beta 1 / 公测版 1** (`v0.10.26-beta.1`).

## 新玩家快速安装

1. **准备游戏和备份存档。** 安装本体和黄金树幽影 DLC，先确认原版可以正常启动，再退出游戏。此公测基线为 1.17.1，其他版本未验证。
2. **下载完整整合包。** 打开本项目公测发布页，在 Assets 中下载 `ELDEN_RING_NIGHTTIDE_v0.10.26_Public_Beta_1.zip`。`SHA256SUMS.txt` 用于核对下载；两个 Source code 附件不是游戏包。完整 ZIP 已包含本版资源，不要再装之前的测试补丁。
3. **安装 ME3。** 打开 [ME3 官方下载页](https://github.com/garyttierney/me3/releases/latest)，在 Assets 中下载并运行 `me3_installer.exe`，按向导安装。官方教程：[Windows 安装说明](https://github.com/garyttierney/me3/blob/main/docs/user-guide/installation.md)。本整合包不附带 ME3 程序。
4. **完整解压到新文件夹。** 例如 `D:\Mods\NIGHTTIDE`（仅为示例，磁盘不限）。找到解压后包内的 `ModEngine` 文件夹；保留整个包的相对目录，不需要覆盖游戏安装目录，也不要只复制 `regulation.bin`。
5. **双击唯一启动入口。** 运行 `ModEngine/launchmod_eldenring.bat`。脚本先校验文件，成功后调用 ME3 和包内 `nighttide.me3`；该配置默认离线。不要直接从 Steam 启动原版来判断 Mod 是否加载。
6. **首次安装先单独运行本包。** 不要与其他修改参数、地图或事件的整合包混装；本公测没有完成兼容性验收。未解决的战斗问题列在 `KNOWN_ISSUES.md`。

### 常见安装问题

| 提示 / 现象 | 处理 |
| --- | --- |
| `ME3 not found` | 安装 ME3 后重新打开启动脚本。如果仍找不到，在 Windows 的“编辑账户的环境变量”中编辑用户 `Path`，新增实际包含 `me3.exe` 的文件夹，保存后重新启动脚本。添加文件夹路径，不是 exe 文件路径。也可按下方说明使用已有的 `E:\me3` 布局。 |
| `Missing file` / `File mismatch` | 检查是否完整解压、是否混入旧补丁、是否自行修改 INI。将完整 ZIP 重新解压到另一个全新目录，不要从旧包随便补单个文件。 |
| 找不到游戏或 Steam | 先确认 Steam 中的本体和 DLC 已安装、原版能正常启动，再按 ME3 官方安装说明检查游戏识别。不要把 ME3 缺失当成 Boss 修复问题。 |
| 能进游戏，但仍有抓取、处决、模型或音乐问题 | 先对照 `KNOWN_ISSUES.md`；这些多为本版已知问题，重新安装不代表能够修复。 |
| 下载后只有几个 Markdown 文档 | 下载的是 Source code；返回 Releases 的 Assets，下载上面列出的完整玩家 ZIP。 |

## ME3 official download / 官方入口

Use the [official ME3 releases](https://github.com/garyttierney/me3/releases/latest) to obtain `me3_installer.exe`, and follow the [upstream installation guide](https://github.com/garyttierney/me3/blob/main/docs/user-guide/installation.md). The steps above describe this NIGHTTIDE package's launcher; ME3 itself is installed separately.

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
