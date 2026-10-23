# Known Issues / 已知问题

Applies to **v0.10.26 Public Beta 1** (`v0.10.26-beta.1`). This is an experimental public test, not a stable completion of the Nightlord integrations. Packaging cleanup adds no gameplay fixes. No Windows game session was run for this release.

本表适用于 **v0.10.26 公测版 1**。本版开放测试，整合清理不等于完成战斗修复；发布前未运行 Windows 游戏。

| Boss / Area | Current status / 当前问题 |
| --- | --- |
| Dreglord / 垃圾王 | A stagger light can appear, but a light attack does not trigger the critical attack. The player can pass into the **head**. Ground corruption gathering, orb effects in both phases, and white objects in phase two remain unresolved. / 失衡有亮光，轻击仍无法处决；玩家会穿入**头颅**。地面腐败汇聚、两阶段光球和二阶段白色物体仍有问题。 |
| Adel / 大嘴 | Player attachment does not follow the animated mouth through the full grab. F4's follow-mode/attachment combination remains an unaccepted candidate. / 抓取时玩家不能全程跟随嘴部运动，F4 组合候选没有通过验收。 |
| Libra / 山羊 | Abnormal motion amplitude, physical reach/damage, critical attacks, and summon behavior/positions remain unresolved. H1's rollback of the reported F3 proximity-crash change is retained; this does not establish stability. / 动作幅度、物理范围与伤害、处决和疯狂老人召唤位置仍有问题。保留 H1 对 F3 靠近崩溃改动的回退，尚不能据此认定稳定。 |
| Nameless / Heolstor / 不得其名 | Body visibility was reported improved, but the phase-two cape remains incorrect. Some combos lack sound and fail to hit the player. Phase transitions, final health-bar removal, and fog cleanup still need full fight verification. / 主体模型已有恢复反馈，二阶段斗篷仍异常；部分连招无声且打不到玩家。完整阶段切换、战后血条和雾门清理仍待验收。 |
| Gladius / 三狼 | Trigger and battle were reported working, and the 19 removed snake soldiers were confirmed absent. The activation location still lacks a sufficiently obvious light cue. / 触发和战斗已有正常反馈，19 只蛇兵已确认消失；入口仍缺足够显眼的亮光。 |
| Rykard arena / 拉卡德场地 | The F4 candidate retains the wicker/furnace enemy during Rykard's battle and disables it only after Rykard's victory flags. Immediate and reload cleanup still need testing. / F4 候选在拉卡德战中保留柳条人，仅在胜利旗标后清理；当次胜利及重载后的清场仍待测试。 |
| Fulghor / 人马 | A previous dedicated damage increase remains in the build, but acceptable damage has not been established by measured game tests. / 保留此前专属伤害调整，尚无定量实测证明伤害已合适。 |
| Music and sound / 音乐与声音 | Several new bosses still use donor/Elden Ring music routes. Matching Adel, Libra, Fulghor, and the insects to their dedicated Nightreign tracks is incomplete. F4 replaces two missing Heolstor sound IDs with existing same-boss sounds; this is not restoration of all original sound. / 多个新增 Boss 仍使用供体或法环曲目；大嘴、山羊、人马和虫子的黑夜君临专属音乐配对未完成。F4 仅以同 Boss 现有声音替代不得其名的两类缺失音效，未补齐全部原音。 |

## Feedback / 反馈

Use the repository's Issues page. Include the beta/game version, arena, phase, reproducible steps, save/reload behavior, and other mods. For head collision/critical attacks, mouth attachment, attack reach, and missing sounds, short videos are more useful than a single screenshot.

请在仓库 Issues 反馈，并注明公测/游戏版本、场地、阶段、复现步骤、重载结果及其他 Mod。头部碰撞与处决、嘴部跟随、攻击范围和无声音动作请尽量附短视频。
