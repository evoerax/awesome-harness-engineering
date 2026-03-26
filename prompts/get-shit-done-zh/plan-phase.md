# 规划阶段（Plan Phase）

通过集成研究和验证创建可执行的原子任务。

## 流程

```
研究 → 规划 → 验证 → 完成
（最多 3 轮修订循环）
```

## XML 任务结构

```xml
<task type="auto">
  <name>创建登录端点</name>
  <files>src/api/auth/login.ts</files>
  <action>
    用 jose 做 JWT（不用 jsonwebtoken — CommonJS 问题）。
    验证 users 表的凭据。
    成功返回 httpOnly cookie。
  </action>
  <verify>curl -X POST localhost:3000/api/auth/login 返回 200 + Set-Cookie</verify>
  <done>有效凭据返回 cookie，无效返回 401</done>
</task>
```

## 规则

- **每个任务 2-5 分钟** — 更长就拆分
- **精确文件路径** — 不猜
- **内置验证** — 每个任务都有 verify + done 标准
- **fresh context** — 每个 plan 自包含
- **纵向切片** — 端到端，不是横向分层

## 纵向 vs 横向切片

```
✅ 好：Plan 01 — 用户功能端到端（模型 + API + UI）
❌ 差：Plan 01 — 所有模型，Plan 02 — 所有 API，Plan 03 — 所有 UI
```

## 代理

- `gsd-phase-researcher` — 研究技术方案
- `gsd-planner` — 从范围创建详细计划
- `gsd-plan-checker` — 检查计划质量（最多 3 轮）
