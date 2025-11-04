# COMP 163 — Project 2: Character Abilities Showcase

**Author:** Rayner Paulino-Payano  
**Date:** 2025-11-04

> AI usage: This README was generated (and later edited) with the help of an AI.

## Project Overview

This repository contains a small Python project that demonstrates core Object-Oriented Programming (OOP) principles: inheritance, polymorphism, method overriding, and composition. The code models a simple role-playing game (RPG) character hierarchy and a tiny battle system to showcase different class abilities.

## Class Structure

### Inheritance Hierarchy

The project uses the following inheritance structure (children inherit and specialize features from their parents):

- `Character` — base class for all entities
- `Player` — base class for playable characters (inherits from `Character`)
  - `Warrior` (subclass of `Player`)
  - `Mage` (subclass of `Player`)
  - `Rogue` (subclass of `Player`)
  - `Warlock` (subclass of `Player`)
  - `Paladin` (subclass of `Player`)

### Composition

- `Weapon` — demonstrates composition (a "has-a" relationship). A character can possess a `Weapon` instance which modifies attacks.

### Provided Battle System

- `SimpleBattle` — a helper class (marked DO NOT MODIFY) that simulates a one-round fight between two `Character` objects.

## Features & Abilities

Below are the main classes and their responsibilities:

- `Character`
  - `attack(target)` — a basic strength-based attack
  - `take_damage(damage)` — subtracts health (no negative health)
  - `display_stats()` — prints name, health, strength, and magic

- `Player` (extends `Character`)
  - overrides `display_stats()` to include class, level, and experience

- `Warrior`
  - stronger, strength-based `attack()`
  - `power_strike(target)` — higher strength damage

- `Mage`
  - magic-based `attack()`
  - `fireball(target)` — high magic damage

- `Rogue`
  - swift `attack()`
  - `sneak_attack(target)` — large damage when conditions met

- `Warlock`
  - dark/magic `attack()`
  - `shadow_bolt(target)` — high magic damage

- `Paladin`
  - hybrid strength+magic `attack()`
  - `holy_light(target)` — heals the target

## How to run

1. Ensure you have Python 3 installed.
2. Save the project code (if not already saved) — for example `project2.py`.
3. From a terminal, run:

```bash
python project2.py
```

The project may also include unit tests in the `tests/` directory; run them with your preferred test runner (e.g., `pytest`).

## Example output

Running the script (or the demo block under `if __name__ == "__main__"`) will print a short demonstration of characters, their stats, attacks, special abilities, and a simple battle. Example (truncated):

```text
=== CHARACTER ABILITIES SHOWCASE ===
Testing inheritance, polymorphism, and method overriding
==================================================

📊 Character Stats:
Character: Sir Rayner
  Health: 120
  Strength: 15
  Magic: 5
  Class: Warrior
  Level: 1
  Experience: 0
------------------------------
Character: Gandalf
  Health: 80
  Strength: 8
  Magic: 20
  Class: Mage
  Level: 1
  Experience: 0
------------------------------

⚔️ Testing Polymorphism (same attack method, different behavior):

Sir Rayner attacks the dummy:
Sir Rayner powerfully attacks Target Dummy for 10.0 damage!

Gandalf attacks the dummy:
Gandalf casts a spell on Target Dummy for 14.0 damage!

✨ Testing Special Abilities:
Sir Rayner uses Power Strike on Enemy1 for 12.5 damage!
Gandalf casts Fireball on Enemy2 for 21.0 damage!

⚔️ Testing Battle System:

=== BATTLE: Sir Rayner vs Gandalf ===

--- Round 1 ---
Sir Rayner attacks:
Sir Rayner powerfully attacks Gandalf for 10.0 damage!

Gandalf attacks:
Gandalf casts a spell on Sir Rayner for 14.0 damage!

--- Battle Results ---
Character: Sir Rayner
  Health: 106.0
Character: Gandalf
  Health: 70.0
🏆 Sir Rayner wins!

✅ Testing complete!
```

## Notes

- This README focuses on documentation and examples. See the `tests/` directory for unit tests that verify inheritance, method overriding, and special abilities.

--

