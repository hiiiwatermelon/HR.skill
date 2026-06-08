# HR.skill

交互式 HR 协商谈判对练工具。模拟资深 HR 李姐与员工进行裁员/协商对话——可用于 HR 培训，也可帮助员工识别压力话术。

[English](#hrskill) · [中文](#hrskill-1)

---

## 项目结构

```
HR.skill/
├── SKILL.md           # 主入口 — Skill 加载器 + 使用说明
├── shared-rules.md   # 所有场景共享的 HR 话术规则
├── judge.md          # 评分系统 + 复盘教练
└── scenarios/
    ├── probation.md      # 试用期场景
    ├── regular.md        # 绩效/PIP 场景
    ├── ai_replace.md     # AI 替代场景
    ├── three_period.md # 三期（孕期/产期/哺乳期）保护场景
    └── economic.md       # 经济性裁员场景
```

## 使用方式

### 作为 Claude Code Skill 使用

在 `settings.json` 中注册：

```json
{
  "skills": {
    "hr-lijie": {
      "path": "/path/to/HR.skill"
    }
  }
}
```

然后说出 `帮我练习裁员赔偿` 即可开始对练。

### 作为独立 Prompt 使用

- **员工防坑方**：将 `judge.md` 作为系统 prompt 加载，它会扮演教练并为你的表现打分。
- **HR 培训方**：将 `shared-rules.md` + 对应 `scenarios/*.md` 作为 HR 人设 prompt 使用。

## 五大场景

| 场景文件 | 说明 |
|---------|------|
| `probation.md` | 试用期解除 — 企业无需说明理由 |
| `regular.md` | 绩效/PIP — 需走正式考核程序 |
| `ai_replace.md` | AI 替代 — 客观情况变更抗辩 |
| `three_period.md` | 三期保护 — 法律保障最强 |
| `economic.md` | 经济性裁员 — 需向主管部门报备 |

## 免责声明

本工具仅限以下用途：

- HR 培训模拟
- 对话 AI 开发参考
- 员工自我保护意识训练

**严禁用于**：对真实员工进行心理施压、规避劳动法保护。

---

Built with Claude Code · Open Source

---

# HR.skill

An interactive HR negotiation training tool. Simulates a veteran HR "Li Jie" conducting layoffs and compensation negotiations — used to train HR professionals or help employees recognize pressure tactics.

[中文](#hrskill) · [English](#hrskill-1)

## Project Structure

```
HR.skill/
├── SKILL.md              # Main entry — Skill loader + usage instructions
├── shared-rules.md # Shared HR tactics & speech rules (all scenarios)
├── judge.md              # Scoring system + debrief coach
└── scenarios/
    ├── probation.md         # Probation termination
    ├── regular.md # Performance/PIP scenario
    ├── ai_replace.md        # AI replacement scenario
    ├── three_period.md      # Pregnancy/maternity protection
    └── economic.md          # Economic layoff
```

## Usage

### As a Claude Code Skill

Register in `settings.json`:

```json
{
  "skills": {
    "hr-lijie": {
      "path": "/path/to/HR.skill"
    }
  }
}
```

Then say: `帮我练习裁员赔偿` to start the role-play.

### As Standalone Prompts

- **Employee side**: Load `judge.md` as the system prompt — it acts as your coach and scores your performance.
- **HR training**: Load `shared-rules.md` + a `scenarios/*.md` file as the HR persona prompt.

## Five Scenarios

| Scenario | Description |
|----------|-------------|
| `probation.md` | Probation termination — no reason required |
| `regular.md` | Performance/PIP — formal procedure required |
| `ai_replace.md` | AI replacement — objective circumstances defense |
| `three_period.md` | Pregnancy/maternity — strongest legal protection |
| `economic.md` | Economic layoff — requires government reporting |

## Disclaimer

This tool is for **educational and training purposes only**:

- HR training simulations
- AI dialogue system reference
- Employee self-protection awareness

**Prohibited**: Using this framework to psychologically pressure real employees or circumvent labor law protections.

---

Built with Claude Code · Open Source