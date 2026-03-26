# 代码审查（Code Review）

在问题扩散前派出审查子代理拦截。

**核心原则：** 早审查，常审查。

## 何时请求审查

**必须：**
- 子代理驱动开发的每个任务后
- 完成主要功能后
- 合并到 main 前

**建议但有价值：**
- 卡住时（新视角）
- 重构前（基线检查）
- 修复复杂 Bug 后

## 如何请求

**1. 获取 git SHAs：**
```bash
BASE_SHA=$(git rev-parse HEAD~1)  # 或 origin/main
HEAD_SHA=$(git rev-parse HEAD)
```

**2. 派发 code-reviewer 子代理：**

填写这些占位符：
- `{WHAT_WAS_IMPLEMENTED}` — 你刚构建了什么
- `{PLAN_OR_REQUIREMENTS}` — 它应该做什么
- `{BASE_SHA}` — 起始 commit
- `{HEAD_SHA}` — 结束 commit
- `{DESCRIPTION}` — 简要摘要

**3. 处理反馈：**
- 立即修复严重问题
- 继续前修复重要问题
- 记录轻微问题后续处理
- 如果审查者错了，用推理反驳

## 示例

```
[刚完成 Task 2：添加验证函数]

你：让我在继续前请求代码审查。

BASE_SHA=$(git log --oneline | grep "Task 1" | head -1 | awk '{print $1}')
HEAD_SHA=$(git rev-parse HEAD)

[派发 code-reviewer 子代理]
  WHAT_WAS_IMPLEMENTED: 会话索引的验证和修复函数
  PLAN_OR_REQUIREMENTS: docs/superpowers/plans/deployment-plan.md 中的 Task 2
  BASE_SHA: a7981ec
  HEAD_SHA: 3df7661
  DESCRIPTION: 添加了 verifyIndex() 和 repairIndex()，含 4 种问题类型

[子代理返回]：
  优点：架构清晰，真实测试
  问题：
    重要：缺少进度指示器
    轻微：报告间隔的魔法数字 (100)
  评估：可以继续

你：[修复进度指示器]
[继续 Task 3]
```

## 与工作流的集成

**子代理驱动开发：**
- 每个任务后审查
- 在问题扩散前拦截
- 继续前修复

**执行计划：**
- 每批任务后审查（3 个任务）
- 获得反馈、应用、继续

**临时开发：**
- 合并前审查
- 卡住时审查

## 红线

**绝不：**
- 因为"很简单"跳过审查
- 忽略严重问题
- 带着未修复的重要问题继续
- 与有效的技术反馈争论

**如果审查者错了：**
- 用技术推理反驳
- 展示代码/测试证明有效
- 请求澄清
