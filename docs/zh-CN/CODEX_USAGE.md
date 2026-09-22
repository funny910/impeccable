# 在 Codex 中使用 Impeccable

Impeccable 已作为 Codex skill 安装。调用方式：

```text
$impeccable
```

也可以直接指定动作：

```text
$impeccable audit 检查这个页面的无障碍、响应式和性能问题
$impeccable critique 评审这个界面的信息层级和视觉表达
$impeccable polish 打磨这个页面，但保留现有产品结构
$impeccable shape 为新页面先做 UX/UI 方案
```

## 推荐顺序

新项目：

1. `$impeccable init`
2. `$impeccable shape`
3. 实现页面
4. `$impeccable audit`
5. `$impeccable polish`

已有页面：

1. 先读取现有 `PRODUCT.md`、`DESIGN.md` 和页面代码。
2. 使用 `$impeccable critique` 或 `$impeccable audit`。
3. 明确范围后再使用 `$impeccable polish`、`$impeccable layout` 或 `$impeccable typeset`。

不要把 Impeccable 当作后台逻辑、数据库或 API 设计工具；它负责界面结构、视觉系统、交互、无障碍和前端体验。

## React Bits Demo

React Bits 示例应作为独立的 React + Vite 项目维护，不要复制进这个 Fork。

对示例项目的请求应明确给出项目目录，例如：

```text
在 <project-root>/react-bits-demo 中，
用 $impeccable audit 检查移动端布局和动效可访问性。
```

项目级 hook 或 `.impeccable/` 状态文件只在明确需要时加入具体项目，不要写入这个 Fork 的生成输出目录。
