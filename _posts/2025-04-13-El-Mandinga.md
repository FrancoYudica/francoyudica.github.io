---
title: El Mandinga
date: 2025-04-12 12:00:00 -0300
categories: [Computer graphics, game]
tags: [
    game, 
    game jam,
    shaders,
    computer graphics,
    godot]     
description: My submission to the Godot Meetup Argentina Game Jam!

image:
  path: /assets/el-mandinga/game.gif
---

Joined [Godot Meetup Argentina Game Jam!](https://itch.io/jam/godot-meetup-argentina-gamejam). The theme of the game jam was **Creatures of the mountain, the pampas and the river**.

![](/assets/el-mandinga/el_mandinga_banner.png)

The game jam lasted just 3 short days.

We formed a team of six, and I took on the role of lead developer alongside a college friend. The rest of the team included a 2D artist, two 3D modelers (one also focused on texturing), and an animator.

We decided to create a card game inspired by the classic Argentine game [Truco](https://es.wikipedia.org/wiki/Truco_(juego_de_naipes)), where you play against [Mandinga](https://es.wikipedia.org/wiki/Mandinga).

In this project, I led the development and handled the following tasks:
- Implemented the Truco engine as a state machine.
- Created an environment to easily incorporate animations.
- Took the role of Graphics Programmer / Technical artist, by implementing all the shaders and post processing effects.
- Designed the game state system, connecting the Truco engine with in-game events.
- And of course, collaborated with the art team to implement all assets, including textures, models, music, and sound effects.

This game jam was short but amazing. I'm proud of what we were able to pull of with just 3 days of development and 2 programmers.
<!-- Center wrapper -->
<div style="display: flex; justify-content: center; align-items: center; margin: 20px 0;">
  <div style="position: relative; width: 750px; height: 445px;">
    <!-- Thumbnail image -->
    <img id="gameThumb" 
         src="https://img.itch.zone/aW1hZ2UvMzQ2Njg1OC8yMDY5NjQyNS5wbmc=/original/Lmwq%2B1.png" 
         alt="Click to Play" 
         style="width: 100%; height: 100%; display: block;">

    <!-- Play button overlay -->
    <button id="playBtn" 
            style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);
                   padding: 12px 24px; font-size: 20px; cursor: pointer; border: none;
                   background-color: rgba(0,0,0,0.6); color: white; border-radius: 8px;">
      ▶ Play
    </button>

    <!-- Game iframe, hidden initially -->
    <iframe id="gameFrame" 
            src="https://itch.io/embed-upload/13381855?color=000000" 
            frameborder="0" 
            allowfullscreen 
            width="750" 
            height="445" 
            style="display: none;">
      <a href="https://zhamiska.itch.io/el-mandinga">Play El Mandinga on itch.io</a>
    </iframe>
  </div>
</div>

<script>
document.getElementById('playBtn').addEventListener('click', function() {
  document.getElementById('gameThumb').style.display = 'none';  // Hide thumbnail
  this.style.display = 'none';                                  // Hide button
  document.getElementById('gameFrame').style.display = 'block'; // Show game
});
</script>

<br>

<div>
<iframe frameborder="0" 
        src="https://itch.io/embed/3466858?border_width=0" 
        width="550" 
        height="165">
</iframe>
</div>
