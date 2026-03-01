---
title: Il Colpo Mascherato
date: 2026-01-31 12:00:00 -0300
categories: [game]
tags: [
    game,
    game jam,
    2d,
    teamwork,
    playable in website
]
description: Our submission to the Global Game Jam 2026

image:
  path: /assets/il-colpo-mascherato/sample.gif
---

# Il Colpo Mascherato

This project was a true exercise in rapid prototyping and creative collaboration, developed by a diverse, multidisciplinary team of 8. We focused on delivering a polished, playable experience within a strictly limited timeframe of 2 days.

## Play the game

<!-- Center wrapper -->
<div style="display: flex; justify-content: center; align-items: center; margin: 20px 0;">
  <div style="position: relative; width: 750px; height: 422px;">
    <!-- Thumbnail image -->
    <img id="gameThumb" 
         src="/assets/il-colpo-mascherato/sample.png" 
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
            src="https://itch.io/embed-upload/16460354?color=5b050e"
            frameborder="0" 
            allowfullscreen="" 
            width="750" 
            height="422"
            style="display: none;">
      <a href="https://kosogames.itch.io/il-colpo-mascherato">Play on itch.io</a>
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
<iframe frameborder="0" src="https://itch.io/embed/4256738" width="552" height="167"><a href="https://kosogames.itch.io/il-colpo-mascherato">Il colpo mascherato by KosoGames, ZHAMISKA, Benicio Porta, VulpinaRose, Franco Yudica, Renata Galaxias, Quimey Ortiz</a></iframe>

</div>
