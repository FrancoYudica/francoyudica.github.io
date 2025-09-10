---
title: Path Forger
date: 2025-05-20 12:00:00 -0300
categories: [Computer graphics, game]
tags: [
    game, 
    computer graphics, 
    google play store,
    shaders,
    godot]     
description: Hook, dodge, and climb in this challenging vertical arcade platformer.

image:
  path: /assets/path_forger/gifs/easy-rotated.gif
---

![##Path Forger](assets/path_forger/imgs/itch_banner.png)
This endless vertical scroller throws you into a fast-paced action game where every moment is a test of your reflexes and precision. Armed with your trusty grappling hook, you'll swing through tight spots, avoid deadly obstacles, and outrun a rising death wall that never stops. It’s a race against time where momentum is everything—the faster you play, the faster you move.

Perfect for fans of arcade games, grappling mechanics, timed survival challenges, and skill-based platformers. How long can you survive the climb.

I hope you like it!

[Privacy Policy](/path-forger/privacy-policy/)

## Video
{% include embed/youtube.html id='_-zPgV2xms4' %}

## Download

You can find Path Forger on itch and on the play store

[![Play Store download link](https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png){: .dark .w-25 w="200"}](https://play.google.com/store/apps/details?id=com.pathforger.pathforger)

<iframe frameborder="0" src="https://itch.io/embed/2640506?bg_color=150925&amp;fg_color=e8daf6&amp;link_color=40ff89&amp;border_color=443854" width="552" height="167"><a href="https://franco-yudica.itch.io/path-forger">Path Forger by Franco Yudica</a></iframe>


## Technical stuff

There are lots of technical aspects that helped me grow in several fields through this project.

### Graphics programming

The game uses lots of shaders. There are very few elements in the game that were drawn by hand.

- Player skins are 2D SDF (Signed Distance Fields).
- Backgrounds are made with real-time shaders as well.
- There are lots of VFX such as distortions and particles.
- The UI FX transitions are made with shaders.

Post processing effects:
- Motion blur for obstacles.
- HUE shift
- Vignette
- Screen top-bottom distortion

Thanks to this approach, I learned about the importance of branchless shader programming and shader optimization.

### Dynamic level generation

The game features a single mode, which is endless and randomly generated.

To achieve this, there are some predefined *level segments*, each with its own associated difficulty value. Then the level generator picks these segments based on the score. To add variety and a unique feel to each playthrough, the level generator uses a normal random distribution. This way, there is some randomness, but the level segments will have the expected difficulty most of the time.

This approach let me design level segments independently, allowing a more modular structure that is easier to debug and build upon.

### State machines

The game relies heavily on state machines. They are used to implement lots of features and serve as a programming pattern that facilitates code readability and scalability.

#### Player controller

The player controller uses a hierarchy of state machines.

The alive state holds:
- Idle
- Throwing hook
- Translating
- Grabbing

The death state expands to:
- Dead
- Respawning

There is also another state machine used for animations. It's separated from the player controller to provide smooth transitions and more flexibility.

Thanks to this approach, the code turned out to be super simple and modular, allowing me to add and remove features without breaking others.

#### UI and game transitions

The UI might look simple, and visually it is, but the main challenge is that it's integrated with the game.

- If you hook the fist node, you enter and start playing the game immediately and smoothly.
- If you click the customization button, the store opens, but the camera focuses on the player, disables its input, and more.
- If you die, the camera backtracks and you return to the menu.

Since using state machines for the player gave me excellent results, I decided to use them here as well.

#### Google play services

The game uses [Google Play Services](https://developer.android.com/distribute/play-services) for storing data in the cloud with **snapshots**, unlocking **achievements**, and string player scores on **leaderboards**.

#### Dynamic audio

Audio also had a big focus, showcasing the following features:
- Changing the pitch of reached Path Nodes based on the current player speed.
- Menus with different music pitch.
- Backtrack after death changes pitch and speed.