---
layout: page
title: Moonshine Lua Modding Documentation
---

**Create, integrate, and share your own games.**

## Why Moonshine?

Like many programmers, I created a Tetris clone, specifically a *Tetris The Grandmaster* variant. Twenty years ago, this was one of the only ways to experience this arcade-exclusive, Japan-only game at home. Beyond recreation, I saw an opportunity to experiment with features and tweaks the original lacked.

My project, called Jagoris, let players play in the browser and submit game replays to the server for verification. The server would validate each replay and add verified scores to leaderboards, allowing players to watch replays and compete fairly. Unfortunately, it didn't stay online long due to technical limitations and licensing issues.

Over the years, I've watched many others attempt similar projects within the TGM community, each reinventing the wheel with varying degrees of success. Few, if any, successfully implemented robust online and community features alongside the game itself.

**Moonshine is my attempt to address that.** It aims to be a platform that lets anyone create a puzzle game simply (I hope), while providing built-in community features out of the box: player progression tracking, leaderboards, and online replay. No need to rebuild the foundation every time, focus on your game design instead.

---

This documentation is designed for content creators and game designers who want to build and publish their own games on the Moonshine platform using Lua scripting. While Moonshine was originally built for puzzle games, it's now flexible enough to support many types of games, including challenging puzzles, roguelike adventures, progression-based challenges, and more.

This guide covers the entire process, from designing your game mechanics to integrating progression systems, building interactive menus, and publishing your creation to the Moonshine community.

## Getting Started

New to Moonshine modding? Start here:

1. **[Introduction]({% link introduction.md %})** - Learn what Moonshine modding is and what you can create
2. **[Getting Started]({% link getting-started.md %})** - Set up your development environment and create your first mod

## Core Concepts

Master the key features of Moonshine modding:

- **[Variations & Modes]({% link variations-and-modes.md %})** - Design multiple game variations, difficulty tiers, and parallel game modes
- **[Menus & Configuration]({% link menus-configuration.md %})** - Create interactive menus and let players customize their experience before playing
- **[Progression System]({% link progression-milestones.md %})** - Build progression paths using milestones to unlock content and gate features
- **[Leaderboards]({% link leaderboards.md %})** - Track player performance and create competitive rankings

## Reference & Examples

- **[Manifest Essentials]({% link manifest.md %})** - Complete technical reference for manifest.json configuration
- **[Best Practices & Edge Cases]({% link best-practices.md %})** - Design patterns, guidelines, and how to avoid common pitfalls
- **[Complete Example: Tower Climber]({% link example-progression-mode.md %})** - Full working example with variations, menus, progression, and leaderboards

## Quick Navigation

| Section | Purpose |
|---------|---------|
| Introduction | Understand what's possible |
| Getting Started | Set up your environment |
| Core Concepts | Learn key features |
| Reference | Look up technical details |
| Examples | See working code |

---

**Last Updated:** January 2026

