# Universal Coding Standards Skill

A language-agnostic coding standards skill for AI coding agents (opencode, Claude Code, Codex, etc.). It defines universal best practices for code quality, safety, dependency management, and project conventions — applicable to any project in any programming language.

## Skill

The skill is defined in `.agents/skills/universal-coding-standards/SKILL.md` and covers:

- **Communication & Runtime Text** — runtime strings in plain English, no emoji
- **Dependency Management** — never modify dependencies without authorization, verify before assuming library availability
- **Safety & Security** — no destructive commands, no secret exposure, ask when uncertain
- **Code Quality & Conventions** — study existing code, follow project conventions, preserve comments, explain *why* not *what*
- **Process & Planning** — no unsolicited planning documents, prefer clarity over cleverness

Rules are classified as **Mandatory** (must follow; violations should block merge) or **Recommended** (strongly encouraged; exceptions need justification).

## Structure

```
.
├── .agents/
│   └── skills/
│       └── universal-coding-standards/
│           └── SKILL.md          # Skill definition and rules
└── .gitignore
```

## Usage

Copy the skill into your AI coding agent's skills directory. The YAML frontmatter in `SKILL.md` includes a `description` field that agents use to auto-trigger this skill when tasks involve code quality, coding standards, conventions, or best practices.

The rules are tool-agnostic — they apply regardless of which agent or IDE you use.
