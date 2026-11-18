# Build With AI — the spec-driven agent workflow

**Stop prompting. Start specifying.**

Six skills that take any project from a vague idea to a shipped, verified
product — discovery, scope cutting, PRD, technical spec, verified build, and
public launch.

[MIT licensed](LICENSE)

---

## The problem

Most AI coding sessions fail the same way: the idea is vague, the scope never
gets cut, context resets between sessions, and the agent "says it's done"
without proof. You end up with code you can't ship and no idea what you're
missing.

This is a workflow that fixes all four.

## The pipeline

| Skill | Produces | What it solves |
|---|---|---|
| **1-start** | `learner-profile.md` | Learns your background and experience so later steps are calibrated to you |
| **2-scope** | `scope.md` | A flipped-interaction interview that pulls the idea out of your head and cuts it to a proof of concept |
| **3-prd** | `prd.md` | The core journey, every behavior, states, edge cases, and a firm scope boundary. No code talk |
| **4-spec** | `spec.md` | The technical blueprint: stack, where it runs, components, data model, file structure |
| **5-build** | working code | Ordered build steps, each verified and committed before the next one starts |
| **6-ship** | public repo + submission | Proof-of-concept verification, demo video script, public repo, written submission |

## Why it works

**Context is never lost.** Each skill reads the previous skill's artifact from
disk. You don't re-explain the project in every new session.

**Scope gets cut, not expanded.** The hardest part of shipping is saying no.
`2-scope` and `3-prd` exist specifically to do that, and they refuse to
produce a spec until the boundary is firm.

**Verification is structural.** `5-build` commits only after a step passes.
`6-ship` verifies the whole thing before anything goes public. "It says it's
done" is never the only evidence.

**The learner profile carries through.** `1-start` writes a profile of your
technical background and goals; every later skill reads it and calibrates
itself accordingly. Beginners get more scaffolding. Experienced builders get
less hand-holding.

## Install

Into OpenCode (all projects):

```bash
git clone https://github.com/omar11-ai/build-with-ai-skills.git ~/.config/opencode/skills
```

Per project:

```bash
mkdir -p .opencode/skills
cp -r skills/* .opencode/skills/
```

Claude Code and Codex follow the same convention — drop the `skills/` folder
into the equivalent skills directory.

## Use

```
/1-start    # -> writes learner-profile.md
/2-scope    # -> writes scope.md
/3-prd      # -> writes prd.md
/4-spec     # -> writes spec.md
/5-build    # -> builds, tests, commits each step
/6-ship     # -> verifies, packages, writes submission
```

Run them in order. Each one expects the previous one's file to exist.

## What's inside

```
skills/
  1-start/   SKILL.md + learner-profile template
  2-scope/   SKILL.md + scope template
  3-prd/     SKILL.md + prd guide + prd template
  4-spec/    SKILL.md + spec patterns + spec template
  5-build/   SKILL.md + code tour + checklist template
  6-ship/    SKILL.md
```

Plain Markdown. No runtime, no dependencies, no license keys, no telemetry.

## Requirements

Any agent client that supports skills (OpenCode, Claude Code, Codex) — or any
LLM workflow that can read Markdown files and write files to disk.

## License

MIT — see [LICENSE](LICENSE).

---

Built by [Omar Wael](https://github.com/omar11-ai).
