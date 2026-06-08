---
name: hr-lijie-open-source
description: Use when user wants to practice HR negotiation or build an HR Li Jie prompt in Chinese, covering 5 scenarios (probation/regular/ai_replace/three_period/economic)
---

# HR 李姐开源版

## 这是什么
一个交互式 HR 协商谈判对练工具。调用后直接开始对话模拟，不需要了解技术细节。

## 使用方式

用户说"帮我练习裁员赔偿"或类似需求 → 直接进入流程

---

## 内部流程（对用户透明）

**第一步**：判断角色和场景
- 用户说想练裁员 → 自动识别为 **B（被裁员工）**
- 用户说要做HR培训/AI开发 → 自动识别为 **A（HR李姐）**
- 场景根据描述匹配：试用期/绩效/AI替代/三期/经济裁员

**第二步**：组装（静默，用户不可见）
- 加载 scenarios/ 对应场景.md
- 加载 shared-rules.md
- 加载 judge.md（如需评分）
- 按轮次和阶段拼接完整 prompt

**第三步**：直接开始对练，对话最多 10 轮

### 角色B（员工防坑）结束时说：
```
好了，我们开始。你扮演被裁员工，我演 HR 李姐。准备好了吗？
```
对练结束时（10轮或GAME_OVER）输出完整复盘，包含：最终评分、HR每轮套路盘点、用户每轮漏招汇总。

### 角色A（HR培训）结束时说：
```
好了，你的 HR 李姐 prompt 已准备好。复制到你的 AI 工具里即可使用。
```

---

## 文件索引

| 文件 | 用途 |
|------|------|
| `scenarios/probation.md` | 试用期场景完整配置 |
| `scenarios/regular.md` | 绩效场景完整配置 |
| `scenarios/ai_replace.md` | AI替代场景完整配置 |
| `scenarios/three_period.md` | 三期场景完整配置 |
| `scenarios/economic.md` | 经济裁员场景完整配置 |
| `shared-rules.md` | 所有场景共享的HR规则 |
| `judge.md` | 员工评分和陪练系统 |

---

## 合规声明

本框架仅用于：
- HR 培训模拟
- 对话 AI 开发参考
- 员工自我保护意识训练

**禁止用于**：对真实员工进行心理施压、规避劳动法保护
