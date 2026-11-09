# COR3 Pillar Skill

给 Codex 和其他 Agent 用的 COR3 推号手册：接手已登录账号后，顺着做完当前能做的剧情、委托、Game Center 日常（DAILY OPS）、市场 REP、Echoes 和配装远征，盯着界面确认到账才算完；踩到攻略没写的坑记进共享库，有实际刷新或冷却时间再约下一轮。

## 开始使用

1. 准备一个能操作浏览器的 Agent，你自己先登录好 [COR3](https://cor3.gg/)。
2. 想让插件帮忙自动解固定小游戏（Decrypt / ICE Wall / Simple Decrypt），按 [COR3 Helper 项目说明](https://github.com/Femtoce11/cor3-helper)装好，只打开你允许的开关。
3. 需要点浏览器工具栏、扩展弹窗或切 Windows 原生窗口时，再接入 [agent-desktop](https://agent-browser.dev/desktop)，提前看清 Windows 下的平台限制。
4. 把仓库里的 `cor3-pillar` 文件夹放进 Agent 的 skills 目录，或者让支持从 GitHub 安装的 Codex 直接执行：

   > 安装这个 Skill：https://github.com/RedeatI/cor3-pillar-skill/tree/main/cor3-pillar

5. 以后更新版本时，拉取最新仓库，把整个 `cor3-pillar` 目录（包含 `references`、`templates`、`agents`）整包覆盖到原安装目录。

开跑时可以直接把下面这段话发给 Agent：

> 使用 $cor3-pillar，先读本账号进度，把当前能做的剧情、市场委托、DAILY OPS 和 Echoes 都做了。按我给的预算和插件开关来，禁开 Auto Job、禁重置、买东西前先查重；遇到拿不准的委托，只要余额和接单名额够、留足已承诺支出就先接了试。等剩下的线都有了明确卡点或冷却，再按游戏里显示的刷新时间约下一次单次运行。收尾关掉游戏标签页，浏览器和登录状态留着。

要不要自动续办、先接未知任务、花钱买配装或开插件开关，全按你自己的授权来。不用 Codex 的 Agent 直接读 [SKILL.md](cor3-pillar/SKILL.md) 就行，按它自己的浏览器和定时接口去跑；这个 skill 本身是一份纯文本操作手册，需搭配外部 Agent 运行。

## 版本历史

版本号对应仓库里的 Git 标签，日期为该版首次提交的北京时间。

### [v1.4.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.4.0) · 2026-11-09 · Echoes 每日双线

- 每天逐号查一遍 Echoes of Planetside 的 A/B 和 C 两条线：两支各至少做掉 1 个可接任务，已经开放的旧章节当轮顺手补完；和 Game Center 里的普通 DAILY OPS 分开记。
- A/B 和 C 分开写当前章节、完成结果和卡点，再去 MR-7 对一遍已解锁和已发现的碎片数。旧兑换码失效时照样看任务和碎片算不算进 The Pillar，兑换码仅限自用，严禁写入记录。
- 写明游戏 3.104.9 的版本变化：Code C 碎片改为随对应任务解锁，取消了日历等待；A/B 现版怎么刷新、到底要不要等满 31 天仍待验证，只按游戏界面真显示的刷新或冷却时间约下一轮。
- 补全从首版到 v1.4.0 的版本历史，并打上 Git 版本标签。

### [v1.3.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.3.0) · 2026-11-09 · Echoes 进度与市场解锁

- 新增 Echoes 操作说明：记录去 RM7-S4L2 拿 `USSDP-V1250_Rep.AD64` 装进 MR-7，以及翻 News、The Pit 论坛帖、历史新闻和 July 线补做旧章节的实测路线。
- 逐个排查 HOME、D4RK、SOYUZ、USOL 四个市场：把“地图上搜到节点”“路线不通”和“能打开 Market 看到 Jobs 列表”分开记，并把各市场状态和 Echoes 进度写进会话模板。
- 实测笔记补入 4 类实战坑：图纸解密后要访问游戏内浏览器 metadata 地址再汇报；远征付款按钮灰先查引导和风险条款勾选；日常面板挡住委托卡片导致打不开时先收起面板再走 Info → Complete；买完 CPU 安装总提示先关机时的单次关机与换装确认顺序。

### [v1.2.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.2.0) · 2026-11-09 · 黑市与市场 REP

- 新增黑市入口、路线和权限排查：连上服务器、能打开 Market、能进受保护文件是三件事，各市场的 REP/CRL 跟账号 Renown、余额、累计收入分开记。
- 剧情或商店软件被市场等级锁住时，优先刷对应市场的 Jobs；交单后盯住 REP、奖金和押金变化，跨过门槛再回去重查商店和卡住的剧情。
- 会话模板增加逐市场记录表，分别记开放状态、市场 REP/CRL 与 XP、下一解锁门槛和差额、可用/在跑委托以及各自独立的刷新时间。

### [v1.1.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.1.0) · 2026-11-09 · 实战执行与续办

- 扩大每轮扫描范围，覆盖已接限时委托、剧情对话/邮件/文件、远征结算、各市场、日常和待领奖励；点完操作等界面反馈、余额或列表真变了再走下一步，列表刷新后按任务名和文件重新找卡，补齐确认弹窗和账面核对，防止漏领奖和重复扣款。
- 补全未知任务策略（允许时先接再探）、卡点排查与安全重试、按资源黄条和供电余量配装（以关机系统通知为准，别单看静态 `POWER ON` 标题）以及远征分步核账；收尾关游戏页留浏览器和登录，再按真实刷新、截止或远征时间约下一次单次运行。
- 新增后台控制、实战踩坑汇总、共享知识库约定、问题与会话模板，以及 Codex 的技能显示配置。

### [v1.0.0](https://github.com/RedeatI/cor3-pillar-skill/tree/v1.0.0) · 2026-11-07 · 首版

- 发布 COR3 Pillar skill 和安装指南，覆盖查看当前剧情、日常、市场委托以及 The Pillar 条件核对。
- 定下工具分工：浏览器控制负责读面板和接交任务，COR3 Helper 只辅助用户允许的固定解谜，agent-desktop 负责工具栏、扩展面板和原生窗口补位。
- 定下收尾记录和验收规则：把声望、累计收入、余额、完成项、卡点和下次可做时间分开记，看游戏界面真到账或状态更新才算完成。

## 参考与模板

- [执行流程](cor3-pillar/SKILL.md)
- [黑市入口、REP 刷级与各市场解锁](cor3-pillar/references/market-reputation.md)
- [Echoes of Planetside 路线、每日双线与碎片核对](cor3-pillar/references/echoes.md)
- [实战踩坑汇总：配装、路线、远征与界面](cor3-pillar/references/field-notes.md)
- [后台控制与界面卡顿排查](cor3-pillar/references/background-control.md)
- [共享实战知识库约定](cor3-pillar/references/knowledge-base.md)
- [问题记录模板](cor3-pillar/templates/problem.md) · [本地会话模板](cor3-pillar/templates/session.md)

本机路径、账号/profile 映射、原始进度和登录凭据留在本地工作目录；复制模板过去填写，个人会话资料切勿提交到公共仓库。

## 适用范围

这里整理的是几个号实战跑出来的经验，还没跑完从零号一路冲到 The Pillar 的全程。文档里记的价格、软件 Power 和节点路线只对应当时测过的样本；游戏改版后目标门槛、活动要求和档位优惠随时可能调，开跑前看一眼你眼前的游戏界面就行。

[COR3 Helper](https://github.com/Femtoce11/cor3-helper) 是第三方插件，网页更新后随时可能失灵；开关显示 ON 之后，还是要回游戏看谜题到底解没解过。Windows 下就算连着后台或传了 `background:true`，操作时仍可能把窗口拉到前台，换了浏览器或机器先做一次只读测试。Skill 本身是一套操作手册，跑起来要靠你自己的模型额度、控制工具和授权，具体能推多快、几天能毕业，以各号实际进度和本地环境为准。

## 工具来源

- [COR3](https://cor3.gg/) · [COR3 社区攻略](https://wiki.mistarg.cn/index.php/COR3)
- [COR3 Helper](https://github.com/Femtoce11/cor3-helper)
- [agent-desktop](https://agent-browser.dev/desktop) · [Windows 支持范围](https://agent-browser.dev/desktop/platforms/windows)

本仓库原创文字采用 MIT 许可证。游戏、插件和其他工具分别遵循其自己的条款与许可证。
