---
title: BomberPibe
date: 2023-12-30 12:00:00 -0300
categories: [game]
tags: [
    game, 
    godot,
    pixelart,
    2d,
    playable in website]     
description: BomberPibe is a 2D platformer with a unique double jump mechanic using your own exploding head.

image:
  path: /assets/bomber-pibe/preview.gif
---

![##BomberPibe](assets/bomber-pibe/banner.png)

BomberPibe was my very first project in Godot. I created it in my university's programming club, working alongside another programmer, an artist, and a music producer. This was the first time I collaborated with a team, and it was an amazing experience, learning how to coordinate, share ideas, and bring a vision to life together. While attending classes, we developed this game as a side project, experimenting with the engine and having a lot of fun along the way.

![](assets/bomber-pibe/animation.gif)

BomberPibe also marked a turning point in my development journey: it was the first time I truly used a game engine instead of building everything from scratch, giving me the foundation to approach future projects with more structure, creativity, and teamwork.


## Play the game

<!-- Center wrapper -->
<div style="display: flex; justify-content: center; align-items: center; margin: 20px 0;">
  <div style="position: relative; width: 750px; height: 445px;">
    <!-- Thumbnail image -->
    <img id="gameThumb" 
         src="https://img.itch.zone/aW1hZ2UvMjQ0NjQxNi8xNDUwMTE1Ny5wbmc=/original/89g%2FdO.png" 
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
            src="https://itch.io/embed-upload/14959260?color=11050d" 
            frameborder="0" 
            allowfullscreen 
            width="750" 
            height="445" 
            style="display: none;">
    </iframe>
  </div>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
  document.getElementById('playBtn').addEventListener('click', function() {
    document.getElementById('gameThumb').style.display = 'none';
    this.style.display = 'none';
    document.getElementById('gameFrame').style.display = 'block';
  });
});
</script>

<br>


<iframe frameborder="0" src="https://itch.io/embed/2446416?bg_color=3a2140&amp;fg_color=caebe0&amp;link_color=4b974f&amp;border_color=42363e" width="552" height="167"><a href="https://clubdeprogramacion.itch.io/bomberpibe">BomberPibe by Club De Programación, Franco Yudica, KosoGames</a></iframe>