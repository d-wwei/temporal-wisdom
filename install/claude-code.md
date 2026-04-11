# Install — Claude Code

## Quick install

```bash
# 1. Inject core rules into CLAUDE.md (direct content injection — works on all versions)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/CLAUDE.md` (appended) | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/temporal-wisdom/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/temporal-wisdom/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/temporal-wisdom/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules (inject directly into CLAUDE.md)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md

# 2. Skill files
mkdir -p ~/.claude/skills/temporal-wisdom
cp SKILL.md ~/.claude/skills/temporal-wisdom/
cp anti-patterns.md ~/.claude/skills/temporal-wisdom/
cp examples.md ~/.claude/skills/temporal-wisdom/

# 3. (Core rules already injected in step 1)
```

## Verify

Ask Claude Code: "What are the temporal wisdom cognitive rules you're following?" It should list the five sections from `cognitive-protocol.md`: identify compound direction, recognize the phase, detect nonlinear thresholds, extend the evaluation window, output self-check.

## Stacking with other cognitive bases

Temporal Wisdom operates on the time dimension of decisions. It does not conflict with First Principles (input quality), Tacit Knowledge (output quality), or Second-Order Thinking (consequence mapping). All load independently.

## Uninstall

```bash
# Remove the Temporal Wisdom section from ~/.claude/CLAUDE.md (search for "# Temporal Wisdom — Cognitive Protocol" header)
rm -rf ~/.claude/skills/temporal-wisdom
```
