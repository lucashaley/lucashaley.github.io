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

_This is very prototype. Please ignore everything about the visuals. You know the drill._

The idea of the game is that you're a drone operator in deep space. You've got to send your drone into an abandoned spaceship (the "husk"), to try to retrieve as much of the data core as you can before the ship collapses, taking your drone with it.

### Key Points

*   I didn't want to have any shooting, or projectiles. Yet, at least. I wanted a relatively non-violent game.
    
*   I really like push-your-luck mechanics. The husk is going to collapse at some point, but you're not sure when. Should you explore further? Or cut your losses and return to the exit?
    
*   I wanted to have different sized 'rooms', but didn't want to bother with complex mapping or generative stuff. It's kept simple, but hopefully still works narratively and conceptually. It might get a little non-Euclidean.
    
*   I wanted to be able to ramp up functionality. So right now, I've got the ship moving around, collecting things, and the Husk has a timer. It's fun, even now. I'd like each pass to keep that fun, and build on it.

<video width="538" height="964" src="https://github.com/lucashaley/lucashaley.github.io/blob/main/uploads/scavenger_03.mp4"></video>

# Turf

Ahh, Turf. This is a big dream of mine -- perhaps too big. Maybe that's why I'm digging a _much_ smaller functional scope with Husk.

![](/uploads/Turf_01.png)

The idea of Turf is that it's a **real-time, real-world mobile strategy game**. 4-10 people start the app, it divides them into two teams, and starts a timer. Then the players run around in the real world, placing virtual markers. The app then uses those markers to create Voronoi zones -- and the most area owned over the longest time is the winner.

There's a lot to go wrong of challenging stuff there.

### Matchmaking

First, we need to host a game, and know when people join the game. There's a good history of matchmaking behaviors there already -- but in this case, we're teaming _by location_. That is, if more than one person is in roughly the same spot, they become a team. And wow, that's when things get interesting. Because what if they move? Who is the "key" person on the team? How far apart can they be before they become a team? With only two teams available, what happens to people outside of those two keys? What if the two teams are too close to each other? Fun stuff.

![](/uploads/Turf_01.jpg)

### Real-time data

It's a real-time game. So the data needs to be real-time, too. For the prototype I used Google's Firebase Realtime databases, which has observer patterns built in. Nice. After wading through setting it all up, and understanding the best nosql data format, it actually works pretty well.

The tricky part comes with parsing that data and creating the Voronoi regions, and ultimately the score. I tried pushing the computations to each client, but found there was some concurrency issues. I'm now in the thick of trying it on the server, using JavaScript server scripts, but man I'm not enjoying it.

# Turbs

A prior keep-it-simple game, that somehow I made totally not simple at all.

# Kyoto

Virtual Japanese gardening.