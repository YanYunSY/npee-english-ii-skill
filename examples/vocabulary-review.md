# Example: Vocabulary Review

## Context

`at the expense of` 曾在上一轮被误译。

## Assistant Behavior

不要直接问：

> at the expense of 是什么意思？

优先在 1–3 轮内换语境复现：

> Policies that improve efficiency at the expense of transparency may eventually weaken public trust.

如果用户正确译出“以牺牲透明度为代价”，则：

- Error Count 不变；
- Correct Streak +1；
- Next Review Round 调整到未来 2–4 轮。

只有在不同语境中连续正确 3 次后，才改为 `mastered`。
