---
title: By Other Means
date: 2020-04-25 17:00:00 -07:00
categories:
- Frustration
- Programming
excerpt: Code with your brain, not your fingers
splash_image: "/uploads/8577ce92-fbd3-4770-a070-8e2ada58c164.png"
posts:
- _posts/2022-01-04-how-to-create-a-new-unity-template-from-scratch.md
layout: post
---

Sometimes I find myself beating my head against a particular programming problem, trying to force the code, and inevitably it means I'm not thinking in the right way about it. It's like the Blaise Pascal quote:

> I have made this longer than usual because I have not had time to make it shorter.

In this most recent incident, I've been trying to code seasonal cycles into a game, in which the various variables could be manipulated per-object, per-season, with custom seasons per-object. Don't ask. Anyways -- here I was, beating my head against modulos and switch cases for a day and a half. Then, on a rare run, I got far enough away from the computer to remember that Unity has [AnimationCurves](https://docs.unity3d.com/ScriptReference/AnimationCurve.html), which basically tick all the boxes could want. It took about 14 lines of code to get to work.

![](/uploads/a5472c51-8a4c-44c5-b959-9629191983e3.png)

It's just a nice reminder that sometimes the best coding is done with your brain, not your fingers, away from the computer.
