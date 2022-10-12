---
layout: post
title: Turf! Classes and Accessibility
excerpt: A mobile game with mobility
categories:
- Accessibility
- Programming
splash: "/uploads/screen-shot-2022-10-11-at-5-42-07-pm.png"
similar_pages:
- _posts/2022-10-07-turf.md

---
One of the first points of interest that came up when designing Turf! was how, as a mobile game that requires movement in physical space, it would be designed so that most people would be able to use it.

Again, the premise is that real people run around real space, and using the game, place virtual markers at real locations which create virtual territory, overlaid on real space. The highest aggregated rate of territory wins.

> It was immediately obvious that people who are fast on their feet would have an advantage. And also that people who are not mobile would not be able to participate in the game at all.

### Player Classes

There is clearly nothing I could do about the relative speeds of players. Runners gonna run. But here is where I could lean on the RTS genre conventions to help out -- player "classes". When joining a game, each player selects a class, that provides certain abilities and restrictions. For the first pass, I included:

* Scout. This class has the most markers to place, and can place them without a long delay. But each marker doesn't last very long.
* Tank. With the fewest markers to place, and the longest placement time, this class shines as those markers last the longest.
* Commander. Fewer markers, and quite a long placement time. But the Commander also has the extra ability to see the opposing team players' locations at all times -- other classes can only see opposing team players' locations when they are in friendly territory.

![](/uploads/screen-shot-2022-10-11-at-5-54-26-pm.png)

Hopefully you can see how these classes and extra abilities help soften the imbalance from physical advantages. Further classes will include:

* Ghost. The mirror to the Commander -- remains invisible at all times.
* Leech. Few markers of their own to place, but can "drain" enemy markers and take them over.
* Drone. Not sure what to call this one, but this class would effectively allow a player to participate without physically moving. Instead, they would send a virtual "drone" to specific locations to place markers. But if that drone gets caught in enemy territory, it's lost.

### System UI

It was also important to me to use system UI as much as possible. That way I could get the most built-in support for voice commands and other accessibility features.

Visually, I'm trying to keep the UI clean, with high contrast, and large, easily readable text. Because for this game, I can. So that's good.