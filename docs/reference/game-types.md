---
title: "BMGD Game Types Reference"
description: All 24 game type templates available in BMGD's Game Design Document workflow
---

# BMGD Game Types Reference

BMGD's GDD workflow includes 24 game type templates. Each template provides specialized guidance for designing that specific genre.

---

## Action Games

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **Action Platformer** | Jump, run, and overcome obstacles | Movement system, combat, level design patterns, ability unlocks |
| **Fighting** | One-on-one combat between characters | Move sets, combo systems, balance, frame data |
| **Shooter** | Combat through projectiles | Weapon systems, aim mechanics, enemy AI, level flow |
| **Survival** | Stay alive in a hostile environment | Resource management, crafting, base building, threat systems |

---

## Adventure & Exploration

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **Adventure** | Narrative-driven exploration | Story structure, puzzles, environmental storytelling, progression |
| **Metroidvania** | Explore an interconnected world with ability-gated progression | Map design, ability gates, backtracking rewards, power curve |
| **Horror** | Evoke fear and tension | Atmosphere, threat design, resource scarcity, pacing |
| **Visual Novel** | Branching narrative with character focus | Story branches, character arcs, dialogue systems, choices |

---

## Strategy & Tactics

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **Strategy** | Real-time or turn-based resource and unit management | Economy, tech trees, unit balance, map control |
| **Turn-Based Tactics** | Small-scale combat with positional strategy | Unit abilities, cover systems, action economy, mission design |
| **Tower Defense** | Defend against waves of enemies | Tower types, enemy variety, placement strategy, upgrade paths |
| **MOBA** | Team-based competitive combat with hero progression | Hero design, laning, item systems, team synergy |

---

## Role-Playing Games

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **RPG** | Character progression through story and combat | Character builds, skill trees, equipment, encounter design |
| **Roguelike** | Procedural generation with permadeath | Run structure, unlock persistence, balance across runs, item pools |

---

## Simulation & Management

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **Simulation** | Model real-world systems | System depth, feedback loops, complexity management |
| **Sandbox** | Open-ended play with user creativity | Toolsets, creation tools, sharing systems, emergent gameplay |
| **Idle/Incremental** | Progress through automated systems | Prestige mechanics, balance curves, offline progression, unlock structure |

---

## Puzzle & Logic

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **Puzzle** | Solve challenges using logic | Puzzle mechanics, difficulty curve, hint systems, variety |
| **Text-Based** | Gameplay through prose input | Parser design, world modeling, narrative integration, hint design |

---

## Sports & Racing

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **Sports** | Simulate competitive sports | Sport rules, player stats, team AI, progression |
| **Racing** | Compete to finish first | Track design, vehicle physics, handling feel, progression |

---

## Other Genres

| Game Type | Description | Key Elements |
|-----------|-------------|--------------|
| **Card Game** | Gameplay through card mechanics | Card design, deck building, RNG management, meta evolution |
| **Party Game** | Multiplayer mini-games for social play | Minigame variety, accessibility, party size support, replayability |
| **Rhythm** | Synchronize actions to music | Beat mapping, difficulty scaling, music integration, visual feedback |

---

## Using Game Type Templates

When you run the `create-gdd` workflow, the Game Designer agent will:

1. Help you select the appropriate game type for your concept
2. Load the specialized template for that type
3. Guide you through type-specific design considerations
4. Generate a GDD tailored to your chosen genre

**Example:** If you select "Action Platformer," your GDD will include:
- Movement system design (jump mechanics, air control)
- Combat system design (attack types, combos)
- Level design patterns (platforming challenges, checkpoint placement)
- Player abilities and progression

---

## Hybrid Types

Many games combine multiple game types. The Game Designer can help you:

1. **Identify your primary type** — The core gameplay loop
2. **Select secondary types** — Systems borrowed from other genres
3. **Balance the combination** — Ensure systems work together

**Examples:**
- **Action-RPG** — Action Platformer + RPG
- **Survival Horror** — Survival + Horror
- **Rogue-lite** — Roguelike + (another genre)
- **Tower Defense RPG** — Tower Defense + RPG

---

## See Also

- **[Workflows Reference](./workflows.md)** — All BMGD workflows
- **[Agents Reference](./agents.md)** — Learn about the Game Designer agent
- **[Set up Unity/Unreal/Godot](../how-to/setup-unity.md)** — Engine-specific setup guides
