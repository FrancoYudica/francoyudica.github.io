---
title: Tethering Faith
date: 2024-01-07 12:00:00 -0300
categories: [game]
tags: [
    game, 
    game jam,
    shaders,
    computer graphics,
    dialogue system,
    ui,
    godot,
    pixelart,
    2d]     
description: My first-ever game jam!

image:
  path: /assets/tethering_faith/game.gif
---

Joined the [New Year New Skills Game Jam!](https://itch.io/jam/new-year-new-skills-game-jam)

The game jam lasted 7 days, 07 - 14 of January.

![](/assets/tethering_faith/banner.png)

Me and a friend from college decided to join an international team. At the time, I had never participated in a game jam or made a game with non-Spanish speakers.

Turns out we could communicate easily, and we decided to create a 2D side-scroller puzzle and narrative-driven gothic pixel game called [Tethering Faith](https://franco-yudica.itch.io/tethering-faith).

Our team consisted of two programmers (including myself), a 2D artist, a composer, and a sound designer.

I took the role of lead developer and was responsible for designing the game architecture, mainly focusing on:

- **Dialogue system**: For learning purposes, I chose to implement a custom dialogue system. It featured my first real and “big” finite state machine, used to handle dialogue transitions and game events.
- **Dialogue text generation with deterministic sounds**: I developed a system that simulates character voices by playing vowel sounds based on the letters in the dialogue text. The system uses deterministic rules to map vowels to pre-recorded sound clips, creating the illusion of speech while maintaining consistency across playthroughs.
- **NPC and characters system**: Implemented all the NPCs, their unique interactions and events.
- **Quest system**: Made a simple inventory based quest system.
- **Graphics**: Implemented all the game shaders, cameras and parallax backgrounds.
- **UI**: Implemented all the game UI.
- **Game state management and event system**

After the jam ended, I shared the project with my *Formal Languages and Computability* professor. She was impressed by the FSM and automata implementations and later invited me to give a talk at my college about finite state machines and their applications in game development.

<iframe frameborder="0" src="https://itch.io/embed/2468334?bg_color=000000&amp;fg_color=c6e4eb&amp;link_color=ae1abe&amp;border_color=333333" width="552" height="167"><a href="https://franco-yudica.itch.io/tethering-faith">Tethering Faith by Franco Yudica, Futotori, KosoGames, Sage901, TheBlackSolace</a></iframe>
