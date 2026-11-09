# COR3 Pillar Skill

给 Codex / 其他 Agent 使用的 COR3 实战流程：推进当前可做内容，核验提交和奖励，探索攻略之外的卡点，并把经验积累到共享知识库。

## 开始使用

1. 准备能控制浏览器的 Agent，自己登录 [COR3](https://cor3.gg/)。
2. 需要插件解谜时，按 [COR3 Helper 项目说明](https://github.com/Femtoce11/cor3-helper)安装，使用你明确允许的开关。
3. 需要工具栏、扩展面板或原生窗口操作时，再接入 [agent-desktop](https://agent-browser.dev/desktop)，并核对平台限制。
4. 将仓库中的 `cor3-pillar` 文件夹安装到 Agent 的技能目录，或让支持 GitHub 技能安装的 Codex 执行：

   > 安装这个 Skill：https://github.com/RedeatI/cor3-pillar-skill/tree/main/cor3-pillar

5. 已安装旧版时，更新仓库并将整个 `cor3-pillar` 目录重新同步到原安装位置，包含 `references`、`templates` 和 `agents`。

开始时可以告诉 Agent：

> 使用 $cor3-pillar，读取本账号进度，完成当前能做的剧情、委托、日常和活动。按我已有的预算与插件授权执行，不用 Auto Job、不重置、不重复购买。不确定的任务在余额与名额允许且留足已承诺支出时先接再探索。剩余事项都存在具体阻碍后，按实际刷新时间安排已授权的下一次单次运行，减少无效检查；结束关闭游戏页，保留浏览器和登录。

是否自动续办、接未知任务、购买设备或使用插件，以使用者自己的授权为准。其他 Agent 可直接读取 [SKILL.md](cor3-pillar/SKILL.md)，使用自身支持的控制和调度接口；skill 不会自行提供后台服务。

## 版本历史

版本号按既有 Git 提交补标，日期为该版功能首次提交的北京时间。

### [v1.4.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.4.0) · 2026-11-09 · Echoes 每日双线

- 每日逐号检查 Echoes of Planetside 的 A/B 和 C，两支各完成至少一项可做任务，已开放的历史章节当轮补完。普通 DAILY OPS 另记。
- 分别记录两支的章节、完成结果和阻碍，并核对已解锁与已发现的碎片数。旧兑换码失效时，仍核对任务与碎片是否计入 The Pillar。
- 记录游戏 3.104.9 取消 C 碎片日历等待的版本差异。A/B 刷新节奏与 31 天耗时仍待验证，续办按游戏实际显示的时间安排。
- 补录首版至今的版本历史，并加上 Git 版本标签。

### [v1.3.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.3.0) · 2026-11-09 · Echoes 进度与市场解锁

- 增加 Echoes 操作指南，记录 News、Forum、MR-7 活动磁盘及补做历史章节的实测路径。
- 逐个核对 HOME、D4RK、SOYUZ、USOL 的市场访问，区分地图发现、路线受阻和实际打开，并把市场与 Echoes 进度写入会话记录。
- 收录图纸解密后的汇报、远征付款按钮、委托详情被面板遮挡、换装后核对强度四类实战问题。

### [v1.2.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.2.0) · 2026-11-09 · 黑市与市场 REP

- 新增黑市入口、路径和权限排查。各市场的 REP/CRL 与账号 Renown、余额、累计收入分别记录。
- 当市场等级卡住剧情或软件时，优先做对应市场委托，提交后核对 REP、奖励和押金，达到门槛再检查商店与剧情。
- 会话模板增加各市场等级、XP、解锁条件、阻碍和刷新时间。

### [v1.1.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.1.0) · 2026-11-09 · 实战执行与续办

- 扩充每轮检查范围，覆盖已接限时委托、剧情、远征、市场、日常及待领奖励。操作后等待界面反馈，核实提交和到账再记进度。
- 补充未知任务、卡点探索、配装、远征结算和后台操作流程。按实际冷却、截止时间或远征结果安排下一次单次续办，收尾关游戏页并保留登录。
- 加入后台操作参考、共享知识库维护规则、问题与会话模板，以及 Codex 的技能显示配置。

### [v1.0.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.0.0) · 2026-11-07 · 首版

- 发布 COR3 推进 skill 和安装指南，覆盖剧情、日常、市场委托和 The Pillar 条件核对。
- 明确浏览器控制、COR3 Helper 固定解谜与 agent-desktop 窗口操作的分工。
- 建立进度记录与验收流程，分别记录声望、累计收入、余额、已完成任务、阻碍和下次可做时间。

## 参考与模板

- [执行流程](cor3-pillar/SKILL.md)
- [黑市入口、REP 委托循环与解锁条件](cor3-pillar/references/market-reputation.md)
- [阶段性实测：配装、路线、佣兵和界面问题](cor3-pillar/references/field-notes.md)
- [后台控制与卡顿排查](cor3-pillar/references/background-control.md)
- [共享知识库维护约定](cor3-pillar/references/knowledge-base.md)
- [问题记录模板](cor3-pillar/templates/problem.md) · [本地会话模板](cor3-pillar/templates/session.md)

本机路径、账号/profile 映射、原始进度和凭据不属于公共技能内容。把模板复制到自己的本地工作目录，再填写实际入口；不要将个人会话资料提交到此仓库。

## 适用范围

这是阶段性实践整理，尚未完整验证从零到 The Pillar。历史价格、强度和路线仅适用于记录的样本；目标等级要求、活动条件和优惠均以当前游戏说明为准。

COR3 Helper 是第三方非官方插件，功能可能随网页更新失效；开关显示开启不等于本次解谜成功。浏览器连接、语义点击或 `background:true` 也不保证不抢焦点，应按实际环境验证。Skill 需要模型、控制工具和用户授权，不承诺无人看管、成功率或达标天数。

## 工具来源

- [COR3](https://cor3.gg/) · [COR3 社区攻略](https://wiki.mistarg.cn/index.php/COR3)
- [COR3 Helper](https://github.com/Femtoce11/cor3-helper)
- [agent-desktop](https://agent-browser.dev/desktop) · [Windows 支持范围](https://agent-browser.dev/desktop/platforms/windows)

本仓库原创文字采用 MIT 许可证。游戏、插件和其他工具分别遵循其自己的条款与许可证。
