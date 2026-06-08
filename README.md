# HR.skill

An interactive HR negotiation training tool. Simulates a veteran HR "Li Jie" (李姐) conducting layoffs/negotiations — used to train HR professionals or help employees recognize pressure tactics.

## What's Inside

```
HR.skill/
├── SKILL.md           # Main entry — Skill loader + usage instructions
├── shared-rules.md   # Shared HR tactics & speech rules (all scenarios)
├── judge.md # Scoring system + debrief coach
└── scenarios/
    ├── probation.md      # Probation termination scenario
    ├── regular.md       # Performance/PIP scenario
    ├── ai_replace.md    # AI replacement scenario
    ├── three_period.md  # Pregnancy/maternity protection scenario
    └── economic.md      # Economic layoff scenario
```

## Usage

Import into any Claude Code project that supports custom skills, or use the files directly as prompts in your AI tool of choice.

### As a Claude Code Skill

Add to your `settings.json`:

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

- **Employee side** (防坑练习): Load `judge.md` as the system prompt — it acts as your coach and scores your performance.
- **HR training**: Load `shared-rules.md` + a `scenarios/*.md` file as the HR persona prompt.

## Scenarios

| Scenario | Description |
|----------|-------------|
| `probation.md` | Probation termination — no reason needed |
| `regular.md` | Performance PIP — requires formal procedure |
| `ai_replace.md` | AI replacement — objective circumstances defense |
| `three_period.md` | Pregnancy/maternity — strongest legal protection |
| `economic.md` | Economic layoff — requires reporting to authorities |

## Disclaimer

This tool is for **educational and training purposes only**:

- HR training simulations
- AI dialogue system reference
- Employee self-protection awareness

**Prohibited**: Using this framework to psychologically pressure real employees or circumvent labor law protections.

---

Built with Claude Code · Open Source