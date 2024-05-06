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

Over the last couple of years, however, I can't help but find the name of the company to be just, well… <strong>ironic</strong>. They're shooting in all sorts of directions, trying to be everything to everyone. More power to them, I guess -- except that the different tentacles of the company don't seem to be talking to each other very well. The new packages don't work well with each other. There's no unity of interface, or programmatic approach. It's really sad to me. And makes teaching it so much more difficult.

Anyways, I've been trying to pull apart the new Unity <a href="https://blogs.unity3d.com/2019/10/14/introducing-the-new-input-system/">Input System</a>. It's a catch-all system for collecting user input, from console controllers to touchscreen devices. As such, it's really abstracted out. Dredging through the demo samples, the code is inconsistent and leverages some pretty obtuse C# techniques, which of course makes it that much more difficult to grok and teach. Anyways. THE FUTURE

<h3 style="text-align: start"><strong>Some notes for my own purposes</strong></h3>
<code>PointerManager</code> collects raw input.
<code>GestureController</code> determines swipes and taps. It assigns its own <code>OnPressed</code> to <code>PointerManager</code>'s <code>Pressed</code> methos.
<code>SwipingController</code> parses gestures for functionality. It assigns its own <code>OnSwiped</code> to <code>GestureController</code>'s <code>Swiped</code> method.
