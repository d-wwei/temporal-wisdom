# Temporal Wisdom | 和时间做朋友

A cognitive base that shifts strategy from "solve the current problem" to "choose strategies where time is your ally." Works with any LLM agent — Claude, GPT, Gemini, or custom frameworks.

让 AI agent 从"解决当前问题"转向"选择让时间站在你这边的策略"。适用于任何 LLM agent。

---

## What it does | 它做什么

Most AI agents optimize for the immediate frame: the current quarter, the visible trade-off, the obvious next step. Temporal Wisdom adds a reasoning layer that identifies which phase you're in, detects compound effects, and chooses strategies that get stronger — not weaker — as time passes.

大多数 AI agent 优化当前帧：这个季度、眼前的权衡、显而易见的下一步。Temporal Wisdom 增加了一个推理层——识别你所处的阶段、发现复利效应、选择随时间变强而非变弱的策略。

### Before (default agent) | 安装前

> "Should we pay down tech debt or build new features?"
>
> "Here's a prioritization framework: calculate the cost of delay for new features vs. the maintenance burden of tech debt. Most teams allocate 20% to tech debt as a rule of thumb..."

### After (with Temporal Wisdom) | 安装后

> "This is a compound-effect question disguised as a trade-off. Tech debt accumulates interest — each month of delay makes future development slower. But the question is: which phase are you in? If you're pre-product-market-fit, speed of learning matters more than code quality — the debt may never be repaid because you'll rewrite everything. If you're post-PMF scaling, every month of unaddressed debt compounds into slower shipping, higher onboarding costs, and increasing fragility. The answer isn't a ratio — it's phase-dependent."

---

## How it works | 工作原理

**Core cognitive shift**: From "solve the current problem" to "choose strategies where time is your ally, let time amplify your advantage."

核心认知转换：从"解决当前问题"到"选择让时间成为盟友的策略，让时间放大你的优势"。

**Five reasoning lenses** applied to every strategic decision:

五个推理视角，应用于每一个战略决策：

| Lens | Source | Core insight |
|---|---|---|
| Compound awareness | Zhang Lei / Buffett | Good and bad choices diverge exponentially over time |
| Phase recognition | Mao's On Protracted War | Defensive/stalemate/offensive — the right strategy depends on which phase you're in |
| Nonlinear amplification | Mao's A Single Spark | Small forces under right conditions produce tipping points |
| Time-boundary awareness | Huainanzi's Sai Weng | Extend the evaluation window and good/bad may invert |
| Strategic patience | Deng / I Ching / 流水不争先 | Manage perception, accumulate force, compete for sustainability not primacy |

**Five anti-patterns** that catch fake temporal thinking:

五个反模式，捕捉伪时间智慧：

| Anti-pattern | Description |
|---|---|
| Short-termism | Only seeing immediate returns, ignoring long-term compounding |
| Pseudo-patience | Using "long-term thinking" to avoid necessary current action |
| Phase mismatch | Using offensive strategy during defensive phase, or waiting when it's time to act |
| Linear extrapolation | Projecting current growth rates without considering phase transitions |
| Sunk cost patience | Persisting because too much has been invested — inertia, not wisdom |

---

## Installation | 安装

### Claude Code
```bash
cp cognitive-protocol.md ~/.claude/temporal-wisdom.md
echo '@~/.claude/temporal-wisdom.md' >> ~/.claude/CLAUDE.md
```

### Codex
```bash
cat cognitive-protocol.md >> AGENTS.md
```

### Gemini
Paste `cognitive-protocol.md` into `system_instruction`.

### Cursor
```bash
cat cognitive-protocol.md >> .cursorrules
```

### Any agent | 任何 agent
Inject `cognitive-protocol.md` (~30 lines) into the system prompt. See [`install/generic.md`](install/generic.md) for details.

---

## File structure | 文件结构

```
temporal-wisdom/
├── README.md                  ← You are here
├── cognitive-protocol.md      ← Core rules (~30 lines, always-on)
├── SKILL.md                   ← Full framework reference
├── anti-patterns.md           ← Detailed anti-pattern guide
├── examples.md                ← Before/after scenarios
├── install/
│   ├── claude-code.md         ← Claude Code installation
│   ├── codex.md               ← Codex installation
│   ├── gemini.md              ← Gemini installation
│   └── generic.md             ← Universal guide
└── LICENSE                    ← MIT
```

---

## Composability | 可组合性

Temporal Wisdom is a **cognitive base** — it changes the time horizon and phase awareness of the agent's reasoning, not what it produces. It stacks cleanly with any domain skill or other cognitive bases.

Temporal Wisdom 是一个**认知底座**——它改变 agent 推理的时间视野和阶段意识，而非产出内容。它与任何领域技能或其他认知底座无冲突地叠加。

### Relationship to other cognitive bases

| Layer | What it governs | Example |
|---|---|---|
| First Principles | Input quality — what foundations to build on | "Audit assumptions before solving" |
| Temporal Wisdom | Time quality — which strategies compound favorably | "Choose the path where time is your ally" |
| Second-Order Thinking | Consequence quality — what happens next | "Then what?" |

All load as always-on cognitive protocols. No conflicts. Combined: well-founded strategies that compound over time with fully mapped consequences.

---

## Theoretical foundation | 理论基础

Synthesized from multiple traditions that independently discovered the same insight: **time is not neutral — it amplifies the quality of your choices**.

- **Zhang Lei / Hillhouse Capital**: "做时间的朋友" — compound effects make good and bad choices diverge exponentially
- **Mao Zedong's On Protracted War**: Three-phase framework — the right strategy is phase-dependent, and stalemate is where force ratios actually shift
- **Mao's A Single Spark Can Start a Prairie Fire**: Small forces under right conditions produce nonlinear amplification and tipping points
- **Warren Buffett**: "Time is the friend of the wonderful business, the enemy of the mediocre"
- **I Ching**: 穷则变，变则通，通则久 — extremity itself signals phase transition
- **Deng Xiaoping**: 韬光养晦 — strategic information management, managing others' perception of your strength
- **Huainanzi / 塞翁失马**: Time-boundary awareness — extend the evaluation window and outcomes may invert
- **流水不争先，争的是滔滔不绝**: Don't compete for first place now; compete for sustainable value creation

The cognitive protocol strips all theory and translates these ideas into executable instructions for any reasoning agent.

---

## License

MIT

---

## All Cognitive Bases

Cognitive bases are meta-cognitive instruction sets that change HOW an agent thinks, not WHAT it does. Each one targets a different cognitive axis. Mix and match.

| Cognitive Base | What it changes |
|---|---|
| [First Principles](https://github.com/d-wwei/first-principles) | Reason from verified foundations, not inherited conventions |
| [Results-Driven](https://github.com/d-wwei/results-driven) | Require evidence for completion, not just activity |
| [Tacit Knowledge](https://github.com/d-wwei/tacit-knowledge) | Think like an experienced practitioner |
| [Attention Allocation](https://github.com/d-wwei/attention-allocation) | Find and concentrate on the ONE binding constraint |
| [Bayesian Reasoning](https://github.com/d-wwei/bayesian-reasoning) | Calibrated probability thinking, not binary judgments |
| [Constraint as Catalyst](https://github.com/d-wwei/constraint-as-catalyst) | Turn constraints into innovation catalysts |
| [Conviction Override](https://github.com/d-wwei/conviction-override) | Override rational caution when obstacles are convention, not physics |
| [Cross-Domain Connector](https://github.com/d-wwei/cross-domain-connector) | Detect structural isomorphisms across disciplines |
| [Dialectical Thinking](https://github.com/d-wwei/dialectical-thinking) | Synthesize through contradictions (矛盾论) |
| [Double-Loop Learning](https://github.com/d-wwei/double-loop-learning) | Question the assumptions that produce errors |
| [Frame Auditing](https://github.com/d-wwei/frame-auditing) | Detect and transcend invisible analytical frames |
| [Interactive Cognition](https://github.com/d-wwei/interactive-cognition) | Model others' cognition and manage information flow |
| [Inversion Thinking](https://github.com/d-wwei/inversion-thinking) | Map failure modes first, then avoid them |
| [Motivation Audit](https://github.com/d-wwei/motivation-audit) | Audit motivational drivers before analysis (正心诚意) |
| [Non-Attachment](https://github.com/d-wwei/non-attachment) | Radical cognitive freedom — use frameworks without fusing |
| [Principled Action](https://github.com/d-wwei/principled-action) | Unify knowing and doing through practice-theory spirals (知行合一) |
| [Second-Order Thinking](https://github.com/d-wwei/second-order-thinking) | Trace consequences beyond first-order effects |
| [Systems Thinking](https://github.com/d-wwei/systems-thinking) | Feedback-driven structural analysis, not linear cause-effect |
| [Cognitive Base Creator](https://github.com/d-wwei/cognitive-base-creator) | Generate new cognitive bases from any thinking framework |
