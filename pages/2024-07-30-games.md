---
title: Games
nav_order: 6
permalink: games
layout: page
---
Here are some personal projects I've been poking at over the years.

# Husk/Scavenger

This is my current whipping post. I've been really inspired by the design philosophy and community of [DragonRuby Game Tool Kit](https://dragonruby.org/) -- not to mention that Ruby is quite nice to code in. It's aggressively goal-oriented, with a lot of what isn't important sloughed off. The premise is to make something simple and fun, and _ship it_. Get it out there. No matter how simple or rough around the edges. So, no 3d, no built-in physics, no fancy render pipelines -- just 1280x720, 60fps 2d simplicity.

![](/uploads/husk_screenshot_01.png)

The idea of the game is that you're a drone operator in deep space. You've got to send your drone into an abandoned spaceship (the "husk"), to try to retrieve as much of the data core as you can before the ship collapses, taking your drone with it.

### Key Points

*   I didn't want to have any shooting, or projectiles. Yet, at least. I wanted a relatively non-violent game.
    
*   I really like push-your-luck mechanics. The husk is going to collapse at some point, but you're not sure when. Should you explore further? Or cut your losses and return to the exit?
    
*   I wanted to have different sized 'rooms', but didn't want to bother with complex mapping or generative stuff. It's kept simple, but hopefully still works narratively and conceptually. It might get a little non-Euclidean.
    
*   I wanted to be able to ramp up functionality. So right now, I've got the ship moving around, collecting things, and the Husk has a timer. It's fun, even now. I'd like each pass to keep that fun, and build on it.
    

# Turf

Ahh, Turf. This is a big dream of mine -- perhaps too big. Maybe that's why I'm digging a _much_ smaller functional scope with Husk.