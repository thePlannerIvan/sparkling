# Sparkling

[![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0-blue.svg)](LICENSE)

**不是一个只会说“您说得太对了”的笔记整理器，而是一个带着材料和你短兵相接的思考对手——专攻用“反常撞击 + PO 挑衅 + 奥卡姆剃刀”陪你打穿业务卡点。**

> 作者：阿祖不看 TVC（小红书同名）· [demyth.info](https://demyth.info) · [Lawyif@163.com](mailto:Lawyif@163.com)

---

## 一句话看懂：它和普通 AI 聊天有什么根本区别？

你把一份复杂问题和背景材料扔给普通聊天窗口，AI 通常会直接给你吐出一篇 1500 字四平八稳的《深度原因分析综述》——读起来每一条都对，合上屏幕一条都没用。

**Sparkling** 制定了一套“高摩擦力共创协议”：

- **首轮拒绝写长公文综述**：一上来直接撕开材料里的**三张张力牌（反常点 / 互斥点 / 被大家默认没检验过的公理）**，和你定锚“到底要解决哪对矛盾”；
- **每轮只打 250 字短兵交锋**：接住你的直觉后，用水平思考 **PO 挑衅**或**冷门事实混成**二选一刺你一下，最后只留**一个尖锐抉择**等你表态；
- **背后有张防倒退白板（`sparkling-whiteboard.md`）**：被硬事实证伪过的假设直接打叉归档，绝不在第 10 轮又悄悄溜回来；需要额外查证外网数据时才会提示补证，绝不现编理由圆谎。

---

## 实际研讨长什么样？（交互流程与两个出口）

```text
你的材料 + 困惑问题
  → 第 1 轮：不废话写综述，直接甩「反常点 / 互斥点 / 默认公理」三张牌
  → 多轮交锋：~250 字短回合（接直觉 → PO 挑衅/混成 → 单点反问）
  → 奥卡姆剃刀剪枝：砍掉“恰好淡季/偶发”类打补丁解释
  → 最终收敛成 2 个实在交付之一：
       ├─ 出口 A：一页纸《Aha! Moment 顿悟纪要》（旧假设为何死 + 新机制 + 停做/转向清单）
       └─ 出口 B：《关键分歧与取证清单》（材料还缺哪条关键事实才敢定案）
```

---

## 什么时候选我 vs 选别的 Skill

| 你的情景 | 用哪个 Skill | 原因 |
| --- | --- | --- |
| 卡在某个业务反常（如“满意度涨了但续费跌了”），手头有点材料想撞破思维惯性 | **本 Skill (`sparkling`)** | 高摩擦、快节奏、共创底层因果解释 |
| 手头是几百条访谈原话/社媒评论，需要全量分门别类并审计正反比例 | [`planners-quali-box`](https://github.com/thePlannerIvan/planners-quali-box) | `quali-box` 负责全量语料编码与可回源研究报告，不适合当轻快头脑风暴 |
| 已经讨论清楚核心判断，要把多家观点整理成整套商业提案 Storyline | [`Planners-Proposal-System`](https://github.com/thePlannerIvan/Planners-Proposal-System) | `Proposal` 内部讨论阶段本身就会调用 `sparkling`，但更重主线组织与工作台交付 |

---

## 快速开始与安装

### 1. 安装

**DSH 用户**：通过 [Planners Form](https://github.com/thePlannerIvan/planners-form) 安装 `planners-proposal-system` 时会一并装好，之后可直接在对话里调用 `sparkling`。

**Codex / Claude Code 用户：**

```bash
npx skills add https://github.com/thePlannerIvan/sparkling --skill sparkling
```

或克隆到本地 Skill 目录：

```bash
git clone https://github.com/thePlannerIvan/sparkling.git ~/.codex/skills/sparkling
# 或
git clone https://github.com/thePlannerIvan/sparkling.git ~/.claude/skills/sparkling
```

*(纯工作流协议 Skill：**不依赖任何脚本或 DSH 插件**；推导卡在缺少外部新事实时，会提示你可选配合环境里的 `/research` 收集原始证据。)*

### 2. 直接这样调用

```text
用 $sparkling 带着这些资料和我讨论：为什么近三个月用户满意度上升，但次月续费率在掉？
先别给我写总结报告，直接用反常和张力和我一轮轮碰撞推导。
```

---

## 目录、协议与商业合作

- **目录构成**：`SKILL.md`（三张张力牌、250 字回合制、PO/混成动作、奥卡姆剃刀、白板维护与两类结案格式）、`agents/openai.yaml`（界面元数据）。
- **许可与归属**：以 [AGPL-3.0-only](LICENSE) 发布；出处见 [NOTICE](NOTICE)，工作白板可留项目标识，最终客户汇报文件默认不带署名；商标边界见 [TRADEMARK.md](TRADEMARK.md)。
- **商业合作**：企业团队共创引导流程定制、战略工作坊支持或闭源授权，请联系 `Lawyif@163.com` 或访问 [demyth.info](https://demyth.info)，详见 [COMMERCIAL.md](COMMERCIAL.md)。
