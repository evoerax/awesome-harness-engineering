# 浏览器测试（QA Browser）

真实浏览器测试 — Agent 能"看到"网页，找到视觉 bug。

## 为什么需要真实浏览器

Claude 是"瞎子" — 它能写代码但看不见网页。真实浏览器给它眼睛。

## 关键区别

| 方案 | 速度 | 状态 | 登录 |
|------|------|------|------|
| 每次新浏览器 | 3-5秒/命令 | ❌ 丢失 | ❌ 重新登录 |
| 持久化 daemon | ~100ms/命令 | ✅ 保留 | ✅ 保留 |

## 命令

```bash
$B goto https://staging.app.com
$B screenshot /tmp/check.png
$B fill @e3 "test@example.com"
$B click @e5
$B text                    # 读取页面内容
$B console                 # 检查 JS 错误
$B network                 # 检查失败请求
$B responsive /tmp/layout  # 3 端截图（手机/平板/桌面）
$B diff https://staging.app.com https://prod.app.com
```

## 流程

1. 在浏览器中打开应用
2. 点击用户流程
3. 每个状态截图
4. 检查 console 错误
5. 检查 network 失败
6. 修复发现的问题
7. 修复后重新验证

## 反模式

- 不截图就测试（没有证据）
- 不检查 console/network（漏掉错误）
- 修复后跳过"重新验证"步骤
