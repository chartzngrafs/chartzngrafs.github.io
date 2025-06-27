---
layout: post
title:  "Using Cursor AI to Build A Navidrome Player App"
date:   2025-06-21 18:34:00 +0000
categories: dev
---

## From Idea to App in 5 Days: Building a Navidrome Player with Cursor AI

I love my self-hosted Navidrome music server, but I’ve always wanted a desktop player that felt made for *me*. The web UI is great. Feishin is tremendous. But, I craved a native Linux app that was fast, feature-rich, and looked good on my desktop. So, I decided to build one. This was my first major coding project, and with the help of Cursor AI, I went from a blank file to a feature-rich app I use daily in about five days.

The project, which I’ve dubbed **[Pyper](https://github.com/chartzngrafs/pyper-app)**, is now a reality on my desktop, and the journey is laid bare in my GitHub commit history. It's a perfect timeline of the learning process.

### Days 1-2: The Foundation and the API Grind

The first couple of days were all about the basics. With Cursor AI as my pair programmer, I started by scaffolding the application with PyQt6. My initial commits were simple: "Initial UI layout," "Add basic Navidrome client integration." It was a slow grind of getting a basic window to appear and then figuring out how to talk to the Navidrome API using `py-sonic`. I spent a lot of time just trying to get a simple list of artists to show up. Cursor was invaluable here, helping generate boilerplate code for the UI and suggesting how to structure the API calls, which saved me from hours of documentation diving.

### Day 3: Making it Usable

By day three, things started to click. I had a breakthrough in displaying albums and tracks in a nested structure. The app started to feel less like a test script and more like a real application. This is when I tackled a key feature: the contextual information panel at the bottom. The goal was to have a dynamic area that showed artist details or album info depending on what you clicked. Getting this to update smoothly without freezing the app was a challenge, but commits like "feat: Implement dynamic contextual info panel" marked a huge win.

### Days 4-5: Aesthetics and Power Features

With the core functionality in place, I spent the last two days on what I really wanted: customization and power features. I went deep on a comprehensive theming system. My commit history lights up with additions like "feat: Add Dracula theme" and the vibrant "feat: Add Synthwave '84 theme." Cursor helped immensely in managing the complex logic for applying stylesheets and, crucially, calculating text contrast to ensure everything stayed readable.

The final push was adding advanced internet radio support. This was the most complex part, involving real-time ICY metadata parsing to grab track titles and a multi-source system to fetch album art from MusicBrainz and iTunes. Seeing the app pull live track info from a radio stream and display the correct album art was the moment I knew Pyper was something special.

### In The End

The result is a Linux-first Navidrome player with powerful search, rich context menus, full queue management, and a theming system that lets me match my mood. Building Pyper was a whirlwind of learning, and I couldn't have done it this quickly without an AI assistant to handle the syntax and boilerplate, letting me focus on bringing my vision to life.