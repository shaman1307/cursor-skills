# cursor-skills

Personal Cursor Agent skills and rules for [shaman1307](https://github.com/shaman1307).

## Layout

| Path | Purpose |
|---|---|
| `skills/paper-report-style/` | Documentation **visual system** only (fonts, colors, layout chrome) |
| `rules/engineering/` | Global programming / collaboration conventions (any repo) |
| `rules/paper-report-style.mdc` | Always-on pointer to the visual skill for docs (MD, HTML, Canvas, …) |

## Engineering rules

| Rule | Idea |
|---|---|
| `verify-on-data` | Measure before claiming root cause |
| `reuse-dont-duplicate` | Search and reuse; don’t fork logic |
| `shared-path-regression` | Touch shared code → verify all consumers |
| `show-plan-before-live-ops` | Plan + explicit go before live mutations |
| `trace-code-to-request` | Blame commit (+ recent chat) before changing intentional shortcuts |
| `hotpath-logging` | No per-item logs without volume estimate |
| `reply-in-chat-not-in-project` | Answer in chat — not comments/UI/docs in the repo |
| `simple-words-summary` | Lead with a plain-language summary before deep detail |

## Install

```bash
git clone https://github.com/shaman1307/cursor-skills.git ~/Git/cursor-skills
mkdir -p ~/.cursor/skills ~/.cursor/rules
cp -R ~/Git/cursor-skills/skills/paper-report-style ~/.cursor/skills/
cp ~/Git/cursor-skills/rules/engineering/*.mdc ~/.cursor/rules/
cp ~/Git/cursor-skills/rules/paper-report-style.mdc ~/.cursor/rules/
```

Optional: paste `skills/paper-report-style/USER_RULES_PASTE.txt` into  
**Cursor → Settings → Rules → User Rules** (account sync).
