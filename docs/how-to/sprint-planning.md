---
title: "Run sprint planning with BMGD"
description: Plan and track development sprints using BMGD's agile workflows
---

# Run sprint planning with BMGD

Plan and track development sprints using BMGD's agile workflows for game development.

---

## When to Use This Guide

- You have a completed GDD and/or Architecture document
- You're ready to start implementing features
- You want to track progress through stories and sprints

---

## When to Skip This

- You're still in the design phase — complete the GDD and Architecture first
- You're doing Quick Flow prototyping — use Indie's quick-prototype instead
- You just want to test a single feature — Quick Dev is faster

---

## Prerequisites

> **Before starting:**
> - BMad Method installed with BMGD module enabled
> - Completed `gdd.md` (Game Design Document)
> - Completed `architecture.md` (Technical Architecture)
> - Basic familiarity with agile/scrum concepts

---

## Steps

### Step 1: Generate sprint status from epics

The Game Scrum Master reads your epic files to create the sprint tracking document.

```
/bmgd-sprint-planning
```

The **Game Scrum Master (Max)** will:
1. Read your GDD and Architecture documents
2. Identify epics (large feature areas)
3. Generate `sprint-status.yaml` with all stories
4. Organize stories into sprints based on dependencies and priority

### Step 2: Review your sprint status

The generated `sprint-status.yaml` includes:

```yaml
sprint: 1
status: In Progress
stories:
  - id: story-001
    title: "Player movement system"
    status: Ready
    priority: P0
    points: 5
    assignee: ""
  - id: story-002
    title: "Basic enemy AI"
    status: Pending
    priority: P1
    points: 8
    assignee: ""
```

Review the stories and adjust as needed:
- **P0** — Must have for this sprint
- **P1** — Should have if time allows
- **P2** — Nice to have, defer if needed

### Step 3: Create detailed stories

For each story, the Game Scrum Master creates a complete story file:

```
/bmgd-create-story [story-id]
```

This generates a story file in `stories/` with:
- **Title** and description
- **Acceptance criteria** — Definition of done
- **Technical notes** — From architecture
- **Test cases** — What needs to be tested
- **Dependencies** — Other stories or systems

### Step 4: Implement stories

Use the Game Developer agent to implement each story:

```
/bmgd-dev-story [story-id]
```

The **Game Developer (Link Freeman)** will:
1. Read the story file and acceptance criteria
2. Reference the architecture for technical guidance
3. Implement the feature with game-specific considerations
4. Create or update tests
5. Mark the story complete when all criteria pass

### Step 5: Review code (when flagged)

When a story is flagged "Ready for Review," use the code review workflow:

```
/bmgd-code-review
```

The Game Developer performs a clean context QA review:
- Verifies acceptance criteria are met
- Checks for performance issues
- Reviews test coverage
- Provides feedback or approves the story

### Step 6: Check sprint status

At any time, check your sprint progress:

```
/bmgd-sprint-status
```

This shows:
- Current sprint number and status
- Story progress (Ready, In Progress, Complete, Blocked)
- Risks and blockers
- Recommended next actions

### Step 7: Close the sprint

When all sprint stories are complete:

```
/bmgd-retrospective
```

The Game Scrum Master facilitates a retrospective:
- What went well
- What could be improved
- Action items for next sprint

Then run `sprint-planning` again to start the next sprint.

---

## What You Get

| File/Folder | Purpose |
|------------|---------|
| `sprint-status.yaml` | Sprint tracking with stories, progress, and risks |
| `stories/` | Folder containing individual story files |
| Each story file | Complete definition with acceptance criteria and tests |

---

## Sprint Workflow Summary

```
sprint-planning → create-story → dev-story → code-review → sprint-status → retrospective
                      ↑_____________|
                      (repeat for each story)
```

---

## Tips

> **Best Practice:** Always generate stories from GDD and Architecture. Don't write stories from scratch — let the Game Scrum Master create complete drafts from your existing documentation.

> **Avoid:** Don't start implementation without stories. Stories keep you focused and provide clear acceptance criteria.

> **Remember:** Every sprint should deliver a playable increment. Test your game after each story completes.

---

## Common Mistakes

| Mistake | Solution |
|---------|----------|
| Writing stories manually | Use `bmgd-create-story` to generate complete stories from GDD/Architecture |
 Starting P2 stories before P0 | Follow priority order — P0 first, then P1, then P2 |
 Skipping acceptance criteria | Each story must have clear "definition of done" before implementation |
 Not testing after each story | Playtest after every story completes — catches issues early |

---

## Story States

| State | Meaning | Next Action |
|-------|---------|-------------|
| **Pending** | Not yet ready to start | Move to Ready when dependencies complete |
| **Ready** | Ready to implement | Run `bmgd-dev-story` |
| **In Progress** | Currently being implemented | Complete implementation or flag if blocked |
| **Complete** | Done and tested | Move to next story |
| **Blocked** | Cannot proceed due to dependency | Resolve blocker or re-plan sprint |

---

## Next Steps

- **[Quick Flow vs Full Production](../explanation/quick-flow-vs-full.md)** — Understand both development approaches
- **[Set up Unity/Unreal/Godot](../how-to/setup-unity.md)** — Engine-specific setup guides
- **[Agents Reference](../reference/agents.md)** — Learn about the Game Scrum Master agent
