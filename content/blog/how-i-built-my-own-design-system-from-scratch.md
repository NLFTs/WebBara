---
title: "From My First Idea to Learning Games: The Process of Making My First Game"
description: A practical guide to my game development workflow, from technical architecture to implementation using Nuxt 3.
date: 2025-04-23
image: https://images.pexels.com/photos/1050312/pexels-photo-1050312.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1
minRead: 10
author:
  name: Marsha Bara Suwarna
  avatar:
    src: https://avatars.githubusercontent.com/u/228843429?v=4&size=64
    alt: Marsha Bara Suwarna
---

After years of being a consumer of digital experiences, I finally took the plunge into game development. Creating a successful web game isn't just about a good idea—it's about building a high-performance engine that feels "native" in a browser environment.

I started by auditing existing web-based games, identifying the common "friction" points that make players lose interest. This revealed a significant gap in performance—most games suffered from long loading screens and stuttering frame rates. For my project, **Squid**, I decided to use **Nuxt 3** and **Nitro** to solve these architectural challenges.

Rather than diving straight into complex assets, I built the game iteratively. I treated the development process like a modular system, documenting each composable and state logic as I went. This created a living framework that allowed the game to evolve without breaking the core experience.

The core of my technical system includes:

- A modular state architecture using **Pinia** for real-time reactivity
- High-performance animation loops using **GSAP** and **Web Workers**
- Server-side logic via **Nitro** for secure data persistence
- A dedicated UI library of responsive Vue components for HUDs and menus

The biggest challenge wasn't the logic itself, but the optimization—learning to offload heavy calculations from the main thread to keep a consistent 60 FPS. But the payoff has been enormous: the game feels incredibly snappy, initial bundle sizes are minimal, and the development workflow is 30% more efficient.

If you're considering building your first web game, my advice is to treat the framework as a modular engine. Start with the core mechanics, optimize your asset delivery, and document your logic as you go. A good game system should empower the player's experience, not hinder it with lag.

I've attached a snippet of my Pinia state management pattern below—feel free to adapt it for your own game project!
