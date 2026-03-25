# Hello World Skill

A sample skill for **The Banana Tool** that demonstrates the basics of the skill interface. Use this as a starting point when building your own skills.

## What it does

This skill registers two commands:

- `/hello [name]` — Says hello. If a name is provided as an argument it uses that; otherwise it falls back to the name configured in settings, or "friend" as a default.
- `/greet` — Returns a random greeting (e.g. "Howdy", "Salutations", "What's up").

## Skill features demonstrated

- **Command handling** — Registering commands and resolving them through the resolver chain (`code`, `skill`).
- **Settings schema** — Exposing a configurable "Your Name" field in the settings overlay so users can personalize greetings.
- **Lifecycle hooks** — Using `initialize` and `cleanup` to run setup/teardown logic.

## Getting started

1. Clone this repo into your Banana skills directory.
2. Install dependencies:
   ```
   npm install
   ```
3. The skill will be picked up automatically by The Banana Tool on next launch.

## Project structure

```
hello-world/
  index.js      # Skill implementation (HelloWorldSkill class)
  package.json  # Package metadata
  README.md     # You are here
```

## Settings

| Key    | Type | Default | Description                          |
|--------|------|---------|--------------------------------------|
| `name` | text | (empty) | If set, greetings will address you by name |

Configure this in **Settings > Hello World** within The Banana Tool.
