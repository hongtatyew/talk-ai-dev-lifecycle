```markdown
---
# Slide 1 — Title
---

# The Minimal AI Development Lifecycle That Works

*Hong · Platform Developer*

---
# Slide 2 — The Problem (Hook)
---

# Sound Familiar?

> *"You got the AI license. So why is the sprint board still the same?"*

- Features/user stories are still vague
- Story points haven't moved — and the Scrum Master and PO are not happy
- Code review load is **heavier**, not lighter
- You're expected to deliver more — but are you?

---
# Slide 3 — The Broken Loop
---

# The Bottleneck Isn't Speed

AI makes you type faster. But that was never the bottleneck.

```
Vague requirement → AI writes something → Wrong thing, fast
```

The real cost is hidden upstream and downstream:

- **Upstream:** No clear spec → AI hallucinates intent
- **Midstream:** No constraints → every developer ships differently
- **Downstream:** No evaluation → bugs reach humans, not AI

> Giving AI to a broken process doesn't fix the process.  
> It just breaks it faster.

---
# Slide 4 — AI Evolution
---

# How We Got Here

```
Prompt Engineering → Context Engineering → Harness Engineering
```

| Stage | What You Do |
|---|---|
| **Prompt Engineering** | Learn to write better prompts |
| **Context Engineering** | Set up AGENTS.md, configure MCPs |
| **Harness Engineering** | Build a system *around* the AI |

> Most teams are still in stage one or two.  

---
# Slide 5 — Harness Engineering
---

# Harness Engineering

A harness wraps around an AI agent to provide four key functions:

| Function | What It Includes |
|---|---|
| **Constrain** | Architectural boundaries, dependency rules, sandboxing, least-privilege permissions |
| **Inform** | Context engineering, documentation, system prompts, runtime policies |
| **Verify** | Testing gates, linters, CI validation, format checks |
| **Correct** | Feedback loops, self-repair mechanisms, agents that fix inconsistencies over time |

---
# Slide 6 — The New Development Lifecycle
---

# AI-Native Dev Lifecycle

```
Bootstrap → Design → Code → Review → Test → Ship
                ↑___________________|
                       (loop)
```

| Phase | Who Does It |
|---|---|
| **Bootstrap** | You + AI (once) |
| **Design** | AI asks, you + your team answer, specs emerge |
| **Code** | AI writes, guided by specs |
| **Review** | AI checks first, human validates |
| **Test** | AI handles unit + integration; you do E2E |
| **Ship** | You |

---
# Slide 7 — Bootstrap Phase
---

# Bootstrap: Set the Stage Once

> The one-time scaffold that makes everything else faster

- Repository structure
- Architecture design 
- CI configuration
- Formatting rules, package manager, app framework

Get this right once — and the AI has rails to run on.

---
# Slide 8 — Design Phase
---

# Design: The AI as Your Thinking Partner

Before any code is written, the agent asks:

> *"What are you really trying to solve?"*

It then:
1. Asks clarifying questions
2. Brainstorms solutions with you
3. Produces a **design document** and **specs** that the agent will later use to write code

---
# Slide 9 — Code, Review, Test
---

# Code · Review · Test

**Code**  
The agent writes code *from the spec* — not from guesswork.

**Review**  
AI reviews before humans do:  
✅ Code quality · ✅ Readability · ✅ Security · ✅ Bug detection

**Test**  
- AI handles: unit tests, integration tests  
- You handle: end-to-end, real-world validation

---
# Slide 10 — Context Drift
---

# The Real Enemy Is Context Drift

The longer a project runs, the more the AI loses the plot.

- Specs go stale
- The AI pattern-matches locally instead of navigating purposefully
- Developers and agents diverge silently

Source: https://openai.com/index/harness-engineering

---
# Slide 11 — The AGENTS.md Trap
---

# The "One Big AGENTS.md" Mistake

Most teams start with one giant instruction file. It breaks in predictable ways:

- Context is scarce — a huge file crowds out the actual task
- When everything is "important," nothing is
- It rots instantly — stale rules, silent drift
- Hard to verify coverage, freshness, or ownership

Early lesson: treat AGENTS.md as a *table of contents*, not an encyclopedia.  
Each file owns one concern. The agent knows where to look.
```
.
├── AGENTS.md                                    ← navigation only
├── ARCHITECTURE.md                              ← system decisions
└── docs/
    ├── specs/
    │   └── YYYY-MM-DD-<topic>-design.md
    └── generated/
        └── db-schema.md
```


Source: https://openai.com/index/harness-engineering

---
# Slide 12 — Introduction to Skills
---

# Skills: Reusable Pieces of the Harness

A skill is a pre-built, composable unit that plugs into any phase of the lifecycle:

| Phase | Skill |
|---|---|
| **Bootstrap** | awesome-copilot/architecture-blueprint-generator |
| **Design** | superpowers/brainstorming, superpowers/writing-plans |
| **Code** | superpowers/subagent-driven-development |

All skills used in this talk are available at:
- https://skills.sh/github/awesome-copilot/architecture-blueprint-generator
- https://skills.sh/obra/superpowers


---
# Slide 13 — The Shift in Engineering Roles
---

# The Shift in Engineering Roles

Harness engineering represents a fundamental change in what software engineers do:

| Before | After |
|---|---|
| AI = faster typing | AI = a system you design |
| More licenses = more output | Better harness = better output |
| One big AGENTS.md | Structured, navigable context |
| Writing repetitive implementation code | Designing architecture, policies, and context |

New core skills: 
- context engineering, 
- policy-as-code, 
- agent orchestration, 
- architecture governance.

---
# Slide 14 — Thanks
---

# Thanks!

```