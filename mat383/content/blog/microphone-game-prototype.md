---
title: "Microphone Game Prototype"
hidecontentbg: false
hidetitle: false
hidesummary: true
hidedate: false
centerdate: true
datelabelupdated: false
date: 2025-03-25T15:53:35+10:00
tags: [game dev]
coverimg: "microphone-game-prototype"
coverimgmaintype: "avif"
hidecoverimg: false
summary: ""
ytvid: ""
smallpost: true
isvideo: true
commentsenabled: true
autoloadcomments: true
draft: false
---


<video src="/videos/now/idontlikeyourface.mp4" controls  preload="metadata" style="box-shadow:0px 0px 35px rgba(200, 200, 200, 0.8)"></video>

<br>

This is an experimental game prototype I made for a uni assignment. In this game, you attack your enemies verbally with insults.

Your words are transcribed offline with the [Godot Whisper](https://github.com/V-Sekai/godot-whisper) plug-in and if you say a word that "offends" the enemy, they take damage. If you don't offend them enough, they get impatient and you lose a life.

It sounded like a fun concept to make, but the big downfall of this game is that the list of offensive words is hand-written and I haven't thought of every single insult in existence. I tried to use AI to generate massive amounts of potentially offensive words, but it just returned words I already thought of plus incredibly specific insults that no normal person would use.

Conversely, I also found that playtesters (myself included) panic and instinctively use the same few cheap insults against every enemy (stupid, fat, ugly, dumb, etc.). I understand why, but it's not interesting gameplay.

One obvious solution to this problem is to evaluate the offensiveness of the player's words using AI. I experimented with this during development but only the smallest large language models were fast enough for near real-time responses. Those were woefully innaccurate, giving wildly different responses for the same inputs and sometimes rambling indefinitely. Lightweight LLM tech would have to get much better to be useful in applications like this, but ngl I'm looking forward to it.

If after all of that you still want to play this game, you can download it [here](https://mega.nz/file/TodxVJrA#hqgzlyt8QB57RuJxmetHqaDuhZDHHG5lbo8P93HLTGU) (Windows only though). You can also find my full dev journal for this game [here](https://v3.pebblepad.com.au/spa/#/public/4jbrj5Mn6wsdGx4qztWhfmZGHr?historyId=fioz49KdVa) (in weeks 1-4).