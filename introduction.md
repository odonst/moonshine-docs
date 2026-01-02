---
layout: page
title: Introduction
---


Moonshine is a platform for building and publishing your own games. Whether you're creating a puzzle challenge, an adventure game, or something entirely unique, Moonshine provides the tools to make it happen.

With Moonshine, you can create [variations and game modes]({% link variations-and-modes.md %}) that let players choose how they want to play, build [interactive menus]({% link menus-configuration.md %}) for player customization, implement [progression systems]({% link progression-milestones.md %}) that gate content based on achievements, and track player performance with [leaderboards]({% link leaderboards.md %}). All of this is configured through a simple JSON manifest and your Lua game logic.

## Additional Information

The platform uses several key components:

- **Lua Scripts** - Your game logic and mechanics
- **Manifest Configuration** - Describe variations, menus, progression, and leaderboards
- **Assets** - Images, sprites, and resources
- **Modder Mode** - Test and iterate without recompiling the engine

## What Can You Create?

### Game Variations & Modes

Create multiple game variants within a single mod:
- **Difficulty levels** - Easy, Normal, Hard, Extreme
- **Game modes** - Survival, Sandbox, Story, Challenge
- **Content packs** - Different themes or rule sets
- **Content tiers** - Tutorial → Practice → Ranked

### Player Progression

Gate features based on player achievements:
- **Locked features** - Show disabled until milestone earned
- **Teaser content** - Show as "coming soon" before unlock
- **Adaptive difficulty** - Unlock harder variations as players progress
- **Unlockable content** - New modes, challenges, rewards

### Player Engagement

Track and display performance:
- **Leaderboards** - Global rankings with custom columns
- **Score types** - Time (Chrono), Points, or Badge-based
- **Achievements** - Milestones earned during play
- **Statistics** - Track custom metrics

## Key Concepts

### Variations
Think of variations as "different ways to play." Each mod has at least one variation. Players select which variation to play.

**Examples:**
- A puzzle mod with variations: "Beginner Puzzles", "Advanced Puzzles", "Daily Challenge"
- A roguelike with variations: "Classic Mode", "Hard Mode", "Permadeath Mode"

### Menus & Configuration
Variations can have menus where players make choices. These choices configure the mode.

**Examples:**
- Difficulty selector (Easy, Normal, Hard)
- Map size (Small, Medium, Large)
- Game speed (Slow, Normal, Fast)
- Nested options (Select difficulty → then select modifiers)

### Progression (Milestones)
Track player progress across sessions using milestones. Gate features based on achievements.

**Examples:**
- "Novice" → "Expert" → "Master" progression
- Unlock harder variations only after beating easier ones
- Show hints ("Complete Easy Mode to unlock...") for locked features

### Leaderboards
Submit scores and track rankings. Display player performance with custom columns.

**Examples:**
- Time-based leaderboards (fastest completion)
- Score-based leaderboards (highest points)
- Multi-column rankings (time + score + badges earned)

## What You'll Need

### Knowledge
- **Lua 5.1** - Programming language for your game logic
- **JSON** - Configuration format (the manifest)
- **Basic game design** - Understanding of game mechanics

### Tools
- **Text editor** - Visual Studio Code, Notepad++, or similar
- **Git** - Version control (optional but recommended)
- **Moonshine Game** - The engine to test your mods

### Files You'll Create
```
my-mod/
├── manifest.json          # Configuration: variations, menus, progression
├── main.lua               # Your game logic
├── SaveState.txt          # Optional: player save data
├── milestones.txt         # Optional: player progression
└── assets/                # Images, sprites
    └── images/
```

## Workflow

1. **Design** - Plan your game mode, variations, and progression
2. **Create Manifest** - Define variations, menus, and structure in JSON
3. **Write Scripts** - Implement game logic in Lua
4. **Test Locally** - Use modder mode to test and iterate
5. **Package** - Prepare your mod for distribution
6. **Deploy** - Share with players

## Next Steps

- **→ [Getting Started]({% link getting-started.md %})** - Set up your environment and create your first mod
- **→ [Variations & Modes]({% link variations-and-modes.md %})** - Learn how to structure variations
- **→ [Menus & Configuration]({% link menus-configuration.md %})** - Build interactive menus

## Quick Example

Here's what a simple mod structure looks like:

**manifest.json:**
```json
{
  "name": "My First Mode",
  "author": "YourName",
  "scriptVersion": "1.0",
  "entryPoint": "main.lua",
  "variations": [
    {
      "id": "easy",
      "label": "Easy Mode"
    },
    {
      "id": "hard",
      "label": "Hard Mode",
      "requiredMilestone": "completed_easy"
    }
  ],
  "milestones": ["completed_easy"]
}
```

**main.lua:**
```lua
-- Your game logic here
print("Welcome to my mod!")
```

That's it! A working mod structure.

## Learning Path

| Level | Focus | Pages |
|-------|-------|-------|
| **Beginner** | Basic setup and single mode | Getting Started → Manifest Essentials |
| **Intermediate** | Variations and menus | Variations & Modes → Menus & Configuration |
| **Advanced** | Progression and leaderboards | Progression System → Leaderboards |
| **Expert** | Complete mod design | Best Practices → Complete Example |

---

**Ready to start?** → [Getting Started]({% link getting-started.md %})

