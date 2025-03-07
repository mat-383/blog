---
title: "Learning Godot in 30 Days (gone wrong)"
hidetitle: false
hidesummary: false
hidedate: false
date: 2025-02-01T12:36:12+00:00
centerdate: true
tags: [ 'game dev' ]
coverimg: "learning-godot-in-30-days"
coverimgmaintype: "png"
summary: "I technically made a game!"
ytvid: "-yiM-IhRL6A"
commentsenabled: true
draft: false
---

# But why

As I've said before, I have always wanted to make games but I never had the patience to learn how to by myself. Now that the semester is over and this website is (mostly) done, I have the perfect opportunity to sit down and do this.

To fast-track this and make interesting content, I'm challenging myself to learn a game engine, specifically [Godot](https://godotengine.org/), and make a decent game with it in a month. I don't normally give myself deadlines like this, but that's the reason I'm still learning this stuff at the age of 21 :P

# My background so far

To give you some context around my current skills, here are the games I've made in the past.

Well... the *presentable* ones.

## Super Pong

This was a group assignment for uni. It's a remake of pong (based off [this tutorial](https://www.youtube.com/watch?v=AcpaYq0ihaM)) where you can move the paddle in any direction. I didn't write much code for this; my job was to make the art assets for it (the main menu is horrid), the particle effects, and the promotional poster. Most of the programming was done by my two other group members.

[(itch.io link)](https://danielpayne.itch.io/super-pong)

{{< youtube hO-UJKaijWg >}}

## Keep Away!

This was also an assignment, but a solo one. It's a short platformer where you have to run away from a ghost that you can slow down by looking at it. It was also based off a [tutorial](https://dev.epicgames.com/community/learning/courses/kna/hour-of-code-unreal-engine-build-your-first-3d-game/0b8a/hour-of-code-unreal-engine-create-your-first-3d-game). I wrote some code (mostly in blueprints), added some features like the ghost, music, and fall faster action, and redesigned the level. I'm sort of proud of this one, but I know I could've done better if I was more familiar with the engine and C++ programming.

[(itch.io link)](https://mat383.itch.io/keep-away)

{{< youtube Ca1IwRTYVj8 >}}

## StealthCraft

Not really a game, but I'm including it for old times' sake. It was a minigame realm (server) for Minecraft Bedrock. It had a long history, opening in 2019 and closing in late 2023. A lot of people worked on it, including myself. I made a lot of things for that community and I learnt a lot of my content creation skills while being there to make better things.

We shut it down because we got too ambitious and didn't have the motivation to finish things when Minecraft Bedrock was such a shoddy platform for developers to work on. I do intend to write about StealthCraft and its' realm more in a future post.

{{< youtube MYckJIZxppU >}}

# Doing tutorials

On December 15th, I started using Godot by following their [official documentation](https://docs.godotengine.org/en/stable/getting_started/introduction/index.html) which has a quick start guide and two simple tutorials in it.

The introduction and step-by-step sections introduced me to some key concepts in Godot and showed me around the engine's editor (I found the option to change the theme to green by myself >:D).

<img src="/images/learning-godot-in-30-days/godot-step-by-step.gif" alt="A GIF of the end result of a tutorial from the Godot documentation, where a placeholder image can be moved around with the arrow keys" loading="lazy" height="321px" width="600px"/>

It had some hands-on sections, but I didn't yet fully understand everything they talked about. That was fine though, the real tutorials were just ahead.

## The 2D one

The 2D tutorial was for a simple bullet-hell game where you dodge enemies and survive for as long as possible.

I finished the tutorial pretty easily. I don't have much to say about it, other than it was pretty simple. Later, I'd like to learn more about how the sprite animations work because I feel like I'll be using those often.

<img src="/images/learning-godot-in-30-days/godot-2d-tutorial.gif" alt="A GIF of the end result of the 2D game tutorial from the Godot documentation, where a player character has to avoid touching enemies" loading="lazy" height="322px" width="600px"/>

## Then the 3D one

The 3D tutorial was for a similar bullet hell game, but in 3D and with a jump mechanic.

I finished this tutorial too. I had a bit of trouble with the player's animation near the end, I just couldn't make the keyframes look as smooth as in the tutorial. Other than that, it went great. Working in 3D wasn't all that different to 2D, but I have a feeling 3D development would be harder with bigger games so I'll stick to making 2D ones after this.

<img src="/images/learning-godot-in-30-days/godot-3d-tutorial.gif" alt="A GIF of the end result of the 3D game tutorial from the Godot documentation, where a player character has to avoid touching enemies and can jump on them" loading="lazy" height="322px" width="600px"/>

After finishing all the official tutorials, I had all of five days left to make my own game. That's right. Because I started this project in the middle of December, I spent a lot of time with my family and procrastinated away the little morsels of time I had left.

# Making my own game

With only five days to work with, I figured I should make a platformer as my first game. It's the typical beginner thing to do.

**On day 1**, I made a new project and tried to make a character and platforms by smacking nodes together. I figured out what nodes to use from the 2D tutorial I finished earlier and some other tutorial online. I gave the player and platforms placeholder textures, then gave the player movement logic by just giving it the default character script template Godot provides.

<img src="/images/learning-godot-in-30-days/godot-day-1.gif" alt="A GIF of a green player character jumping around on platforms with placeholder textures" loading="lazy" height="345px" width="580px"/>

**On day 2**, I learnt how to use make and use a tilemap from the Godot documentation and replaced the platforms with proper terrain.

<img src="/images/learning-godot-in-30-days/godot-day-2.gif" alt="A GIF of a tilemap being laid out in the Godot editor" loading="lazy" height="324" width="500"/>

**Day 3**, I added an angry enemy that walks left and right, bouncing off walls. I made this by copying the player script, removing the input logic, and figuring out how to make the enemy flip it's rotation when it collides with something. It also bounces off the player because I didn't get around to making game over logic.

<img src="/images/learning-godot-in-30-days/godot-day-3.gif" alt="A GIF of a green player character running and jumping around an enemy NPC" loading="lazy" height="285" width="362"/>

I skipped **day 4** because I was busy that day.

**And on day 5**, I let the player bounce on top of the enemies and added a finish flag. Going to the finish flag takes away your controls, puts up a victory screen, and makes the player do small jumps forever. The game *technically* has an ending now.

<video src="/videos/learning-godot-in-30-days/platformer-haha.mp4" controls preload="metadata"></video>

And that's the whole game.

Not too proud of it, but it was fun and satisfying to make a game by myself even if the end result is... that. 

It's obvious what went wrong, I botched several weeks of my time and still only spent a couple hours a day on making the game after that. It was also my first time making content in years, so I was doing all this *while* recording it *and* writing a [video](https://www.youtube.com/watch?v=-yiM-IhRL6A) script *and* this blog post. I'll have to learn to doom-scroll less and better manage those different tasks.

# Downloads

You can download Windows and Linux builds of this game from [here](https://mega.nz/folder/zy4WzBQL#HMD0jEfG13QfAy44yGxFeA). It should work for everyone because it works on my machine ;)

Thanks so much for reading this! In my next post, I will be improving this skeleton of a game and trying to finish it.