# 🔥 Cinder Soul

A 2D platformer game built with Java and JavaFX. Fight through multiple levels, defeat enemies, collect items and survive.

![Java](https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=java)
![JavaFX](https://img.shields.io/badge/JavaFX-17-blue?style=flat-square)
![Maven](https://img.shields.io/badge/Maven-3.8-red?style=flat-square&logo=apachemaven)
![Status](https://img.shields.io/badge/Status-Completed-green?style=flat-square)

---

## 🎮 Gameplay

- Fight through **3 levels** with increasing difficulty
- Switch between **sword** and **bow** weapons
- Defeat **3 types of enemies** with unique behavior
- Collect **item drops** to restore health or boost stats
- Fullscreen support and resolution-independent rendering

---

## ⚔️ Enemies

| Enemy | Behavior |
|-------|----------|
| Slime | Melee attack, follows the player |
| Wizard | Ranged attack, shoots poison projectiles |
| Knight | Slow but deals heavy melee damage |

---

## 🎯 Controls

| Key | Action |
|-----|--------|
| A / D | Move left / right |
| Space | Jump |
| Left Click | Attack |
| Tab | Switch weapon (sword / bow) |
| Escape | Pause menu |
| F11 | Toggle fullscreen |

---

## 🏗️ Architecture

The game is built around an **Entity** base class with inheritance:

```
Entity
├── Player
├── Enemy
│   ├── WizardEnemy
│   └── KnightEnemy
└── Arrow
```

**Key systems:**
- `GameWorld` — main game engine, AnimationTimer-based game loop
- `FrameAnimation` — sprite animation system
- `SoundManager` — Singleton pattern for audio management
- `LevelConfig` — level scaling and enemy configuration
- **Delta time** — frame-rate independent movement (works the same on any hardware)
- **AABB collision detection** — axis-aligned bounding box physics

---

## 🧠 Java Concepts Applied

- OOP — inheritance, polymorphism, encapsulation
- Collections — `ArrayList`, `Iterator` for safe removal during iteration
- Functional programming — Lambda expressions, Stream API
- Design patterns — Singleton (SoundManager), Game Loop (AnimationTimer)
- Exception handling — resource loading (sprites, audio)

---

## 🚀 How to Run

**Requirements:** Java 17+, Maven

```bash
git clone https://github.com/vadimjuggc/cinder-soul.git
cd cinder-soul
mvn javafx:run
```

---

## 👨‍💻 Author

**Vadim Guk** — 2nd year student at BSUIR, Computer Engineering  
[GitHub](https://github.com/vadimjuggc)
