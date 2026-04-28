# planning-skills

A small GitHub-ready repository that packages three Codex planning skills. Each
top-level directory is a self-contained skill that can be installed independently.

- `simple-planning`
- `advanced-planning`
- `gen-todolist`

## Repository Layout

```text
planning-skills/
├── advanced-planning/
│   ├── SKILL.md
│   └── agents/openai.yaml
├── gen-todolist/
│   ├── SKILL.md
│   └── agents/openai.yaml
├── simple-planning/
│   ├── SKILL.md
│   └── agents/openai.yaml
├── README.md
└── .gitignore
```

The flat layout keeps install paths short while still letting Codex install any
skill by directory path.

## Installation

Install all three skills from this repository:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo EveGoodEvening/planning-skills \
  --path advanced-planning gen-todolist simple-planning
```

Install one skill:

```bash
python ~/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py \
  --repo EveGoodEvening/planning-skills \
  --path simple-planning
```

Restart Codex after installing new skills.

## Included Skills

### `simple-planning`

Read the relevant codebase and produce a scoped implementation plan without writing code.

### `advanced-planning`

Compare viable implementation approaches, analyze tradeoffs and risks, and recommend the best plan.

### `gen-todolist`

Turn a task into a detailed Markdown checklist, optionally for writing into a planning document.

## Maintenance Notes

- Keep each skill self-contained in its own top-level directory.
- `SKILL.md` is required for every skill.
- `agents/openai.yaml` is optional UI metadata, but should stay in sync with the
  corresponding `SKILL.md`.
- Avoid adding per-skill README files unless they are intentional bundled
  references used by the skill.
