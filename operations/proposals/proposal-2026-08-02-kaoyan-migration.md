---
title: "迁移考研系统到 Hub"
proposal_id: proposal-2026-08-02-kaoyan-migration
status: applied
created: 2026-08-02
updated: 2026-08-02
summary: "将现有考研项目适配为 Hub 中的 kaoyan 行动轨道，保留原项目不删除。"
---

# 迁移考研系统到 Hub

## 依据

- 用户已于 2026-08-02 明确确认迁移，并要求保留当前项目不删除。
- 当前项目的计划、状态、记录和学科知识边界清晰。
- Hub 已有数学、英语一和 408 Topic，但尚未初始化行动层。
- Hub 中 11 份已摄取来源与当前项目对应文件内容一致，不需要重复摄取。

## 变更

- 创建 `operations/tracks/kaoyan/`。
- 将目标和范围迁入 `GOAL.md`。
- 将稳定学习规则迁入 `STRATEGY.md`。
- 将第一轮安排适配为一份已接受计划。
- 将已确认的 2026-08-01 延期事实写成导入记录。
- 从计划和记录派生 `STATE.md`、`NOW.md` 和 `DASHBOARD.md`。
- 补齐行动层索引并更新 Hub 日志。

## 影响与边界

- 不删除、不移动、不修改原 `kaoyan-system` 项目。
- 不修改已有 raw 来源。
- 计划不是学习事实；没有记录的进度保持未知。
- 政治保持未启用，不进入当前学习主线。

## 回滚

迁移前已生成一次 Hub 快照。Hub 现已启用 Git，后续以 Git 变更集回滚；原考研项目始终保留。

## 应用结果

- 已创建 `kaoyan` Track、第一轮计划、迁移记录和派生状态。
- 已补齐英语一和 408 的综合文章及索引。
- 原考研项目和既有 raw 来源均未修改。

## 来源映射

| 原内容 | Hub 位置 |
|---|---|
| 目标、时间条件和科目边界 | `operations/tracks/kaoyan/GOAL.md` |
| 学习原则、讲解规则、延期和复盘机制 | `operations/tracks/kaoyan/STRATEGY.md` |
| 总体与三科第一轮计划 | `operations/tracks/kaoyan/plans/plan-2026-first-round.md` |
| 当前状态 | `operations/tracks/kaoyan/STATE.md` |
| 2026-08-01 明确延期事实 | `operations/tracks/kaoyan/records/record-2026-08-01-001.md` |
| 数学、英语一和 408 学科体系与详细计划 | 既有 Topic raw 及其编译文章 |
| 原项目说明和工作规范 | Wiki operations 协议与 Track 策略共同承接 |
| 空记录、空政治目录和空来源目录 | 不迁移，不创建占位内容 |
