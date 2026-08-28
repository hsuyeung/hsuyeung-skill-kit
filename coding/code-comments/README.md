# Code Comments

让 AI 少写“看起来很认真、其实只是把代码念一遍”的注释。

这个 Skill 不追求注释越多越好，也不把“只写 why，不写 what”当成绝对规则。它关注的是一个更实用的问题：

> 这条注释有没有保存代码本身无法可靠表达、但未来读代码的人确实需要知道的信息？

## 适合场景

- AI 编写新代码时控制注释质量
- Review diff 中新增或修改的注释
- 清理旧代码里的冗余、过时或误导性注释
- 编写 Docstring、Javadoc、XML Doc、TSDoc
- 检查 TODO / FIXME 是否真正说明了未完成的条件
- 解释 workaround、兼容性限制、业务约束和非显而易见的实现选择

## 核心原则

在添加注释之前，先问能不能通过更好的命名、类型、函数边界或代码结构，让代码自己把意思说明白。

真正值得留下的注释通常是在保存这些信息：

- 为什么选择当前实现
- 业务规则或外部系统约束
- 修改时必须保持的不变量
- API 的调用契约、边界和副作用
- workaround 或兼容性原因
- 看起来可以简化、实际上不能简化的 trade-off
- TODO / FIXME 的明确完成条件

例如，这种注释通常没有价值：

```csharp
// Filter valid orders
var validOrders = orders.Where(x => x.IsValid).ToList();
```

而这种信息即使代码已经很清楚，仍然可能值得保留：

```csharp
// Keep cancelled bookings in the export because the finance system
// uses them to reconcile refunds against the original transaction.
```

## 使用

安装后可以让 Agent 在写代码时自动遵循，也可以显式审查：

```text
使用 Code Comments 审查这次 diff 里的注释。
判断哪些应该保留、重写、删除，哪些应该通过重构代码来消除。
```

真正的 Agent 指令见 [`SKILL.md`](./SKILL.md)。
