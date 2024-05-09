---
published: true
date: 2020-06-05
title: Unity new input system
categories:
  - Unity
  - Frustration
  - Programming
excerpt: A personal note to remind myself
splash_image: /uploads/CodeSample_01.png
---
I'm a big fan of Unity. I've been using it since version 2. I've seen it go from small upstart, Mac-only, working with other small Mac apps like [Cheetah3d](http://cheetah3d.de/), to a behemoth owning a huge chunk of the game dev base, and more. I still use it every day, and teach it in my courses.

Over the last couple of years, however, I can't help but find the name of the company to be just, well… *ironic*. They're shooting in all sorts of directions, trying to be everything to everyone. More power to them, I guess -- except that the different tentacles of the company don't seem to be talking to each other very well. The new packages don't work well with each other. There's no unity of interface, or programmatic approach. It's really sad to me. And makes teaching it so much more difficult.

Anyways, I've been trying to pull apart the new Unity [Input System](https://blogs.unity3d.com/2019/10/14/introducing-the-new-input-system/). It's a catch-all system for collecting user input, from console controllers to touchscreen devices. As such, it's really abstracted out. Dredging through the demo samples, the code is inconsistent and leverages some pretty obtuse C# techniques, which of course makes it that much more difficult to grok and teach. Anyways. THE FUTURE

### Some notes for my own purposes
`PointerManager` collects raw input.
`GestureController` determines swipes and taps. It assigns its own `OnPressed` to `PointerManager`'s `Pressed` method.
`SwipingController` parses gestures for functionality. It assigns its own `OnSwiped` to `GestureController`'s `Swiped` method.
