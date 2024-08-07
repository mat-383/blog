---
title: "Building this website"
hidetitle: false
hidesummary: false
hidedate: false
date: 2024-08-03T04:23:38+10:00
centerdate: true
tags: [ 'website' ]
summary: "Let me tell you why I made it and what tools I used."
commentsenabled: true
draft: false
---

***TLDR:*** *I wanted to get into game development and have a website with a shiny custom domain to blog on. I built it with Hugo and it's being hosted on Cloudflare Pages with a Cloudflare domain.*

# The why

So just like the next guy, I've always had an interest in creating games, programming, and making cool stuff. I just never had the motivation or patience to learn to do those things to a standard that I could be proud of.

About two years ago, I was inspired by some great story-based games I played at the time and had an idea for a game. No, it was more of a hazy vision. It was an ambitious story-based game of my own that I knew I had to make. The thought of playing that game and sharing it with the world captivated me. I started making notes of ideas I had relating to this game and was obsessively thinking about it for months.

But eventually, I came to the realization that this project was way too ambitious for me to do in a couple short years, especially with my lack of experience with proper game development.

So I'll go get some!

<br>

Everyone in the indie game dev community says it's a common mistake for newbies to make their big dream game the first project they work on. They also say you should have an online presence *while* making your games, otherwise you'll be swallowed by the sea of everyone else's indie games. Those both sounded like valid bits of advice so I thought I should spin up a website, start making small games, and document their development online.

*"Why a website though? Can't you just make a YouTube channel like everyone else does?"*

Because I've gotten tired of editing videos. I also didn't find much interest in other people's dev logs on the platform at the time. Writing text-form posts on a website also sounded like a way more convenient way of sharing updates. However, I admit that it would be nigh impossible to get new eyeballs on me without a presence on YouTube, so I will make some posts into videos when I get a good editing workflow going.

# Early attempts (bad)

I started building the website when my ambition greatly outweighed my rusty HTML/CSS skills, Like, massively.

I whipped up this concept in Photoshop. The idea was that the entire website would be themed to resemble the profile picture I use everywhere. Heaps of slow-moving PNGs of soft green circles would make up the background and everything would have graceful animations. It was a neat idea, but if you're familiar with the concept of colour banding and why it ruins gradients, you'd know why this would've been horrible in practice.

<img src="/images/old-mat383-website-concept.jpg" alt="A very old concept of mat383.com" width="550"/>
<span class="figcaption">graphic design is my passion</span>

Then I tried to make that website myself. I never built an entire website before though so I jumped head first into writing static HTML by hand, giving zero thought to how the blog will actually blog.

Yeah don't do that.

<img src="/images/old-mat383-website-prototype.png" alt="A very old prototype of mat383.com" width="750"/>
<span class="figcaption">Well, there's some resemblance</span>

I even tried making that cool animated background I was talking about. I didn't know any Javascript at the time though so I called upon ChatGPT to do it all for me. We really tried, there was a lot of back and forth. The furthest we got is spreading a bunch of PNGs across the screen.

<img src="/images/old-mat383-website-bg-prototype.jpg" alt="An old work-in-progress background for mat383.com" width="750"/>

You can download these scuffed prototypes <a href="/files/mat383.com-prototypes.zip">here</a>.

I came to my senses after all that and stopped trying to make the website like this. I think I dropped the project for about half a year after that.

# What's a web framework??

A while later, I started over from scratch. This time, I'd make the website's backend before the front-end. I did some research on how I could make a blog with Python, the language I was the least inexperienced with. Django seemed like a pretty popular pick, so I looked up some tutorials on how I could do that.

I went through several tutorials but they were all so fast that I didn't understand what the code I was copying did.

<img src="/images/old-mat383-website-prototype-2.png" alt="An old prototype of mat383.com" width="650"/>

I'm not giving download links for these, I'm pretty sure I put my personal password in one of their databases.

<br>

I gave up again for a while, then I stumbled upon <a href="https://landchad.net" target="_blank" rel="noopener noreferrer">landchad.net</a>, a website that has a simple tutorial on how to set up a very basic web server. I decided to follow it and bought the domain [mat383.com](/) from Cloudflare and rented a VPS from Vultr. I bought the domain from Cloudflare because I was convinced they had the cheapest prices and least amount of upselling BS (it was honestly impressive after browsing the sites of other domain name registrars). I chose Vultr for my hosting because that's what the website recommended, but I'd advise against using them now (their support is bad, but more on that later).

After doing their tutorial, I had my very own website!

<img src="/images/barebones-mat383-website.png" alt="Barebones mat383.com" width="500"/>
<span class="figcaption">It IS a website...</span>

It was only three lines of text, but I had a web server running with a domain. That was cool.

I wanted to try using Django again, but properly. <a href="https://www.youtube.com/playlist?list=PLlM3i4cwc8zBRQOGXuLrCLNfpVOuVLuwZ" target="_blank" rel="noopener noreferrer">This course</a> on YouTube was very thorough, way more thorough than the other tutorials I did in the past, but I also had a lot of issues with it. Sometimes they would skip over small details or my configuration would be different to theirs so I spent way more time troubleshooting than following their instructions. It took me almost a month to complete the roughly hour-long course, as I got tired from troubleshooting and took breaks.

<img src="/images/simple-mat383-website.png" alt="Barebones mat383.com" width="600"/>
<span class="figcaption">Not much changed</span>

Then I remembered that course was only for setting up the production workflow of a Django website, I still had to make the website after all that!

# Enter Hugo

Just as I was about to embark on a quest to finally learn Django again, I learnt about the existence of <em style="font-family:serif; font-weight: bold;">static site generators</em>. They are tools that let you build entire static websites using a bunch of well-formatted templates and content files. Since they're static and lightweight, some places like Github and Cloudflare will even let you host them for free! The lack of a backend makes static websites much faster than typical dynamic websites, but they also can't have any server-side logic.

I chose Hugo as my static site generator as I've heard of it before and it didn't seem to hard to learn. Setting it up was much simpler than all the stuff I did with Django. I watched <a href="https://www.youtube.com/watch?v=ZFL09qhKi5I" target="_blank" rel="noopener noreferrer">this YouTube video</a> that explained the basics of Hugo and provided <a href="https://github.com/LukeSmithxyz/lugo" target="_blank" rel="noopener noreferrer">a basic theme</a> for me to use. I modified the theme, some of the templates, and the CSS until I was happy how it functioned and looked.

<img src="/images/recent-ish-mat383-website.png" alt="mat383.com built with Hugo" width="700"/>
<span class="figcaption">An earlier version of this site built with Hugo</span>

<br>

<img src="/images/almost-done-mat383-website.png" alt="mat383.com built with Hugo, almost finished" width="700"/>
<span class="figcaption">The home page at the time of writing</span>

It's not completely finished yet, but I'm quite happy with this website.

I also moved my website off Vultr and onto Cloudflare Pages. I won't have to worry about forgetting to pay for hosting there because it's free.

**EDIT:** I'm going to be moving away from Cloudflare entirely soon. While I don't consider myself a privacy enthusiast (you shouldn't need to be an "enthusiast" to care about your privacy), I want to respect those who do.

# Ok, what now?

Before I start developing games, I want to polish up this website and add a couple features. Adding comment support to this website is my number one priority right now, I wasn't able to finish it in time (I just *had* to write this post on the third day of the eighth month).

I'd also like to join a couple website collections and webrings. I specifically designed this website to be very lightweight so I can get into the <a href="https://512kb.club/" target="_blank" rel="noopener noreferrer">512KB Club</a>. You see, I grew up using a terrible internet connection (5Mbps down, 1Mbps up) with a low-end laptop. I understand why making lightweight software is important. The homepage of my website currently weighs in at about **40KB**, so I should be able to get into the <em class="green">Green Team</em> of the 512KB Club and I can put a neat little green badge in the footer. *Yippeeee!!*