# Known Issues / 已知问题

Applies to **v0.10.38 Public Beta 2** (`v0.10.38-beta.2`). This is an experimental public test, not a stable completion of the Nightlord integrations. Adel grab lock timing and flat-floor leave/reset were checked in play. Libra swing amplitude and Heolstor phase-1 hit feel remain broken, and that work is paused. Other inherited F4 candidates are unchanged from Public Beta 1. Removing backup files from the ZIP does not fix those encounters.

本表适用于 **v0.10.38 公测版 2**。本版仍是开放测试。大嘴抓取锁定时机与平地离场重置已实机核对。山羊挥击幅度与不得其名一阶段打击感仍未修好，相关工作已暂停。其余 F4 继承候选与公测版 1 相同。从 ZIP 去掉备份文件不等于修好这些遭遇。

| Boss / Area | Current status / 当前问题 |
| --- | --- |
| Dreglord / 垃圾王 | Unchanged from Public Beta 1. A stagger light can appear, but a light attack does not trigger the critical attack. The player can pass into the **head**. Ground corruption gathering, orb effects in both phases, and white objects in phase two remain unresolved. / 与公测版 1 相同。失衡有亮光，轻击仍无法处决；玩家会穿入**头颅**。地面腐败汇聚、两阶段光球和二阶段白色物体仍有问题。 |
| Adel / 大嘴 | Grab lock timing and flat-floor leave/reset (F8.4 / F8.4.1) were verified in play. The arena leave zone is 54 m from marker `2054390850`. Full mouth-follow through the animated grab remains the unaccepted F4 candidate and is not confirmed by this check. / 抓取锁定时机与平地离场、重置（F8.4 / F8.4.1）已实机验证；离场区距标记 `2054390850` 为 54 m。全程跟随动画嘴部仍是未验收的 F4 候选，本次确认不包含该项。 |
| Libra / 山羊 | Custom `c7561` bone order does not match stock `c7560`. The F8.6.2 bone-slide and stub retarget are in this package; swing amplitude is still wrong. Work is paused at the owner's request. Reach/damage, critical attacks, and summon behavior remain unresolved from Beta 1. The Beta 1 note on the H1 proximity-crash rollback is unchanged; this cycle adds no new proximity result. / 自定义 `c7561` 与原版 `c7560` 骨骼顺序不一致。F8.6.2 骨骼滑动与 stub 重定向仍在包内，挥击幅度仍然错误，已按所有者要求暂停。攻击范围、伤害、处决和召唤与公测版 1 相同。公测版 1 关于 H1 靠近崩溃回退的说明保持不变，本轮没有新的靠近结果。 |
| Nameless / Heolstor / 不得其名 | Phase-1 combo still has no hit feel or SFX. The P1 anibnd overlay is present; the ERR full model is not used. Work is paused. Phase-two cape, phase transitions, health-bar removal, and fog cleanup remain unverified, unchanged from Beta 1. / 一阶段连招仍无打击感与音效。P1 anibnd 覆盖层仍在，未使用 ERR 完整模型，相关工作已暂停。二阶段斗篷、阶段切换、战后血条和雾门清理与公测版 1 相同，仍未验收。 |
| Gladius / 三狼 | Unchanged from Public Beta 1. Trigger and battle were reported working, and the 19 removed snake soldiers were confirmed absent. The activation location still lacks a sufficiently obvious light cue. / 与公测版 1 相同。触发和战斗已有正常反馈，19 只蛇兵已确认消失；入口仍缺足够显眼的亮光。 |
| Rykard arena / 拉卡德场地 | Unchanged from Public Beta 1. The F4 candidate retains the wicker/furnace enemy during Rykard's battle and disables it only after Rykard's victory flags. Immediate and reload cleanup still need testing. / 与公测版 1 相同。F4 候选在拉卡德战中保留柳条人，仅在胜利旗标后清理；当次胜利及重载后的清场仍待测试。 |
| Fulghor / 人马 | Unchanged from Public Beta 1. A previous dedicated damage increase remains in the build, but acceptable damage has not been established by measured game tests. / 与公测版 1 相同。保留此前专属伤害调整，尚无定量实测证明伤害已合适。 |
| Music and sound / 音乐与声音 | An F9 edit to `cs_smain.bnk` silenced all boss music and was rolled back. This package ships the stock bank (1390900 bytes, SHA-256 prefix `ca3d50f2eadebd0c`). Nightreign OST is not included. Dedicated tracks for Adel, Libra, Fulghor, and the insects remain unshipped. F4's two Heolstor sound-ID substitutions are unchanged. Boss music is not fixed. / F9 修改 `cs_smain.bnk` 曾使全部 Boss 音乐无声，已回滚。本包为原版 bank（1390900 字节，SHA-256 前缀 `ca3d50f2eadebd0c`）。未附带黑夜君临 OST。大嘴、山羊、人马和虫子的专属曲目仍未加入。F4 对不得其名两类缺失音效的替代保持不变。Boss 音乐不能视为已修复。 |

## Feedback / 反馈

Use the repository's Issues page. Include the beta/game version (`v0.10.38-beta.2`), arena, phase, reproducible steps, save/reload behavior, and other mods. For head collision/critical attacks, mouth attachment, attack reach, and missing sounds, short videos are more useful than a single screenshot.

请在仓库 Issues 反馈，并注明公测/游戏版本（`v0.10.38-beta.2`）、场地、阶段、复现步骤、重载结果及其他 Mod。头部碰撞与处决、嘴部跟随、攻击范围和无声音动作请尽量附短视频。
