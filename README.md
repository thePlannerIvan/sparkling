# Sparkling

携带材料，与用户共创业务判断的结构化研讨 Skill。

[![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0-blue.svg)](LICENSE)

作者：阿祖不看 TVC · 小红书同名账号 · [demyth.info](https://demyth.info) · Lawyif@163.com

## 使用方式

调用名：`sparkling`。需要和人一起推导业务卡点、检验假设、寻找洞察。材料不足时不代替调研，也不承诺直接生成确定答案。

从材料中的反常与矛盾出发，明确问题和交付目标；用证据检验解释，持续更新研讨白板，收敛为结论纪要或验证清单。

```text
用 sparkling 帮我讨论这份材料：为什么用户满意度上升，续费却在下降？先一起找解释，不要直接写方案。
```

## 安装

```bash
npx skills add https://github.com/thePlannerIvan/sparkling --skill sparkling
```

也可以克隆到支持 Skill 的 Agent 目录（以下为 Claude Code）：

```bash
git clone https://github.com/thePlannerIvan/sparkling.git ~/.claude/skills/sparkling
```

在 DSH 中，Planners Form 会随调用本组件的配套 Skill 安装它；安装后仍可通过 `sparkling` 独立调用。它没有独立审阅页，不在 Planners Form 设置中单列。

没有脚本运行时或审阅页依赖。需要补充外部证据时可选用环境中的 `research` Skill；未安装时先明确资料缺口。

## 目录

`SKILL.md`：入口、研讨步骤与白板契约。

## 开源与归属

许可文本见 [LICENSE](LICENSE)（AGPL-3.0）。作者和来源见 [NOTICE](NOTICE)，名称使用边界见 [TRADEMARK.md](TRADEMARK.md)，合作入口见 [COMMERCIAL.md](COMMERCIAL.md)。署名用于仓库和工作过程，默认不加入最终客户交付物。
