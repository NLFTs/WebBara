---
title: "From my first idea to Learning games : The process of making my first game"
description: A detailed explanation of my game creation method, from initial research to final delivery, with practical tips for ideas at every stage.
date: 2025-04-23
image: https://images.pexels.com/photos/1050312/pexels-photo-1050312.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1
minRead: 10
author:
  name: Marsha Bara Suwarna
  avatar:
    src: https://avatars.githubusercontent.com/u/228843429?v=4&size=64
    alt: Marsha Bara Suwarna
---

Creating a successful game isn't about selling an idea—it's about developing a creative mindset that adapts to the unique challenges of each project. After refining my approach across dozens of projects, I've developed a process that consistently delivers results while still allowing room for creativity and iteration.

In this article, I'll cover my game creation process, from initial discovery to handover to developers, using my recent work on the Squid app as a case study.

### Phase 1: Discovery & Technical Research
Every great game starts with a loop. For Squid, our challenge was to build a compelling web-based experience that felt snappy and responsive, avoiding the "laggy browser game" stigma.

### User Interviews
I conducted sessions with seven core gamers to understand their habits. A major pain point was "friction"—players hate waiting for long loading screens just to play a quick session.

"I want a game that's fun and accessible instantly, whether I'm on my phone or desktop." — Interview participant

### Tech Stack Benchmarking
I analyzed existing web games and chose Nuxt 3 for its speed and developer experience. By leveraging Universal Rendering, we could ensure the landing pages were SEO-friendly while the game engine ran purely on the client side for maximum performance.

### Defining Success
Before opening VS Code, I set these key performance and engagement metrics:

Performance: Achieve a consistent 60 FPS and a Lighthouse performance score > 90.

Retention: Increase daily active usage (DAU) by 40% via Nuxt-powered push notifications.

Stability: Maintain zero state-desync issues during multi-tab play.

### Phase 2: Ideation & System Architecture
With the mechanics set, I moved into the technical blueprinting of the game.

### Technical Sketching
I started with logic flowcharts to map out the game loop. I mapped out how data would flow from the Nitro server engine to the client-side state.

### Information & Game Architecture
I developed a modular architecture using Nuxt Composables and Pinia:

Core Game Engine — Custom Vue composables managing the game clock and delta time.

State Management — Pinia stores to handle player inventory, XP, and real-time stats.

Server API (Nitro) — Secure endpoints for high scores and player data persistence.

UI Components — A library of reusable Vue components for HUDs, menus, and modals.

Design & Dev Principles
Reactivity First — Use Vue’s reactive() and ref() for instant UI updates when game stats change.

Asset Optimization — Use Nuxt Image to serve compressed sprites and textures.

State Persistence — Sync local game state with the database via Server-Side Middleware.

### Phase 3: Prototyping & Testing
Low-Fidelity Logic (The "Grey Box")
I built a functional prototype using basic HTML shapes to test the math and physics. I used Nuxt DevTools extensively to monitor state changes in real-time.

### Playtesting (Round 1)
Testing revealed technical bottlenecks:

Heavy calculations were blocking the main thread, causing "stutter."

Initial bundle sizes were too large for mobile users.

Mid-Fidelity & Optimization
I refined the tech stack based on feedback:

Moved heavy calculations into Web Workers to keep the UI fluid.

Implemented Dynamic Imports and Lazy Loading for game assets to reduce initial load time.

Integrated Optimistic UI updates so players see immediate results even with high latency.

### Phase 4: Visual Design & Implementation
Visual Language & Micro-interactions
I developed a "Cyber-Retro" aesthetic using Tailwind CSS. I used GSAP (GreenSock) for high-performance animations that don't tax the CPU as much as heavy JS-loops.

### Design System (The UI Kit)
To speed up development, I built a Nuxt-specific component library:

GameHUD.vue — A responsive overlay with auto-scaling typography.

SpriteComponent.vue — An optimized component for rendering animated assets.

GlobalToast.vue — For achievement alerts and system messages.

### Phase 5: Deployment & Iteration
Developer Collaboration & CI/CD
I deployed the game using Vercel with Nuxt’s Edge Side Rendering (ESR) to ensure low-latency API calls for players globally.

### Post-Launch Analytics
We used Nuxt Scripts to integrate lightweight analytics without hurting our 60 FPS target. We monitored:

Player drop-off points in the onboarding flow.

The frequency of specific game-loop interactions.

### Results & Learnings
Six months post-launch, Squid has far exceeded our goals:

52% increase in daily active usage.

78% of users reported the game felt "as smooth as a native app."

The modular Pinia architecture reduced bug reports by 30%.

The most valuable lesson? Nuxt isn't just for websites. By treating the framework as a modular engine, we built a scalable, performant game that proves the web is a first-class gaming platform.
