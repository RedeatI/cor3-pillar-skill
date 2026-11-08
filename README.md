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

## 2026-11-09 更新

- 一轮覆盖剧情、消息、文件、地图、各市场、日常和奖励；解锁新内容后继续推进，按具体阻碍决定何时收尾。
- 点击后等待实际反馈；列表刷新后重新锁定任务，处理确认弹窗，防止重复付款和漏领奖。
- 卡点按可见证据提出假设，合理重试并探索其他路径；未知原因不写成永久不可做。
- 根据资源条、供电和实际软件强度判断配装；保留成功和失败对照，不照搬其他账号。
- 按实际时间单次续办并合并临近检查；多账号共用任务时，只停止已达标账号。
- 多执行者共同维护独立知识条目，保留证据、反例、适用范围和当前结论。

## 参考与模板

- [执行流程](cor3-pillar/SKILL.md)
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
