# COR3 Pillar Skill

一份给 Codex / 其他 Agent 使用的 COR3 操作手册：插件处理固定解谜，AI 推进任务，agent-desktop 补充桌面操作。

## 开始使用

1. 准备能操作浏览器的 Agent，自己登录 [COR3](https://cor3.gg/)。
2. 按 [COR3 Helper 项目说明](https://github.com/Femtoce11/cor3-helper)安装插件，先阅读其非官方工具与账号风险说明。
3. 需要操作工具栏、插件面板或 Windows 窗口时，按 [agent-desktop 文档](https://agent-browser.dev/desktop)安装并接入你的 Agent。它是控制工具，本身不带模型。
4. 将本仓库的 `cor3-pillar` 文件夹安装到你的 Agent 的技能目录，或让支持 GitHub 技能安装的 Codex 执行：

   > 安装这个 Skill：https://github.com/RedeatI/cor3-pillar-skill/tree/main/cor3-pillar

5. 开始时告诉 Agent：

   > 使用 $cor3-pillar，检查我已登录的 COR3 账号，先推进能做的剧情、日常和委托。允许用插件辅助解谜，不启用 Auto Job、不自动卖物品；购买设备前告诉我价格。完成后记录实际收入、声望和卡点。

其他 Agent 可直接读取 [SKILL.md](cor3-pillar/SKILL.md)，并使用它自身支持的工具接口。

## 能做什么

- 盘点等级、声望、累计收入、设备、任务和冷却。
- 按需使用插件支持的自动解密、ICE Wall 和简单解密；检查游戏中的实际结果。
- 推进可达任务，避免在路线不通、维护或前置未解锁时反复尝试。
- 分开记录累计收入与余额，以及限时委托和剧情进度。

## 使用前知道这几件事

Skill 是操作说明，需要你自己的模型额度和控制工具。它不会独立运行，也不承诺无人看管、成功率或达到 Pillar 的时间。当前分享来自阶段性实践，尚未完整验证从零推进到 Pillar。

COR3 Helper 为第三方非官方插件。网页更新可能导致失效，自动化操作可能有账号风险；插件项目声明的全部功能并未在本仓库逐一实测。Windows 最小化、锁屏和需要前台键鼠的操作也存在限制。

编写时的 Pillar 条件为声望 20、累计收入 150 万 CR、完成 Wings of Mars 和完整 Echoes of Planetside。等级优惠以你账号的结算页为准：视频中的“约省 40 美元”对应原价 $79.99 的 Founder 档位五折，不是所有版本固定减 $40。

## 工具指路

- [COR3](https://cor3.gg/) · [Fragmentary Order](https://fragmentaryorder.com/)
- [COR3 Helper](https://github.com/Femtoce11/cor3-helper)
- [agent-desktop](https://agent-browser.dev/desktop) · [Windows 支持范围](https://agent-browser.dev/desktop/platforms/windows)
- [COR3 社区攻略](https://wiki.mistarg.cn/index.php/COR3)

本仓库的原创文字采用 MIT 许可证。游戏、插件和其他工具分别遵循其自己的条款与许可证。
