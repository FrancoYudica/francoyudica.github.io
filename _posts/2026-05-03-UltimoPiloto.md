---
title: Ultimo Piloto
date: 2026-05-03 12:00:00 -0300
categories: [game]
tags: [
    game,
    game jam,
    2d,
    teamwork,
    playable in website,
    godot
]
description: My SciFi game submission to the Godot Meetup Argentina Game Jam II

image:
  path: /assets/ultimo-piloto/sample.gif
---

# Ultimo piloto

I'm quite proud of this project, not so much because of the game jam itself, but mostly because of how the game was built and architected internally. For the last couple of years, I've been studying the use cases of state machines in game development. Using this architecture at my job with [ClubQuest](https://www.clubquest.io/) has already driven incredible improvements, and this game relies heavily on state machines to manage quite literally everything: menus, the player, enemies, projectiles, waves, and more. This keeps the codebase incredibly clean and manageable. For me, this project served as a case study in game architecture and code design, clearly validating the workflow I've been using and proposing at [ClubQuest](https://www.clubquest.io/).

While the game might look simple on the surface, it features a massive number of states for a game jam project. We're talking localization, the game intro, first-wave commentary, mid-wave dialogue, death animations paired with the restart menu, game completion, credits, and more. All of these states are seamlessly managed by the state machine, heavily leveraging the [Godot State Charts](https://github.com/derkork/godot-statecharts) addon. This setup allowed me to create an extensible codebase, which is absolutely fundamental for larger projects.

Architectural patterns aside, I kept working on the game to add some extra polish after the jam wrapped up. I played around a lot with shaders and dynamic post-processing. Sci-fi games are the perfect canvas for adding tons of VFX, and I had so much fun with this one!

## Play the game

<!-- Center wrapper -->
<div style="display: flex; justify-content: center; align-items: center; margin: 20px 0;">
  <div style="position: relative; width: 750px; height: 422px;">
    <!-- Thumbnail image -->
    <img id="gameThumb" 
         src="/assets/ultimo-piloto/sample.png" 
         alt="Click to Play" 
         style="width: 100%; height: 100%; display: block; filter: brightness(25%);">

    <!-- Play button overlay -->
    <button id="playBtn" 
            style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);
                   padding: 12px 24px; font-size: 20px; cursor: pointer; border: none;
                   background-color: rgba(0,0,0,0.6); color: white; border-radius: 8px;">
      ▶ Play
    </button>

    <!-- Game iframe, hidden initially -->
    <iframe id="gameFrame"
            src="https://itch.io/embed-upload/17552809?color=000000"
            frameborder="0" 
            allowfullscreen="" 
            width="750" 
            height="422"
            style="display: none;">
      <a href="https://zhamiska.itch.io/ultimo-piloto">Play on itch.io</a>
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

You can also get it on itch: 
<div>
<iframe frameborder="0" src="https://itch.io/embed/4533068" width="552" height="167"><a href="https://zhamiska.itch.io/ultimo-piloto">Último piloto by ZHAMISKA, Franco Yudica, KosoGames</a></iframe>

</div>
