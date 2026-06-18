# 🎛️ Live Coding Music with Strudel REPL

I started learning how to code music!!! This repository contains a collection of my original (and very beginner-level) musical sketches, rhythms, and generative loops built entirely inside **Strudel REPL**.

❗A little caveat - I've got zero knowledge of music theory. I just play what sounds good to me❗

---

## 🎵 What is Strudel REPL?

[Strudel](https://strudel.cc/) is an open-source, web-based live coding platform that turns JavaScript into a canvas for music theory, sound synthesis, and rhythmic exploration. It brings the power of **TidalCycles** (a famous live coding environment) directly into the browser, meaning you don't need to install any software to start making music with code.

Instead of writing linear music in a traditional timeline (like Ableton or FL Studio), Strudel allows you to describe **cycles of time** using functions and strings. 

### Core Concepts of Strudel:
* **The Cycle:** Time is cyclical. A single string of code represents one full continuous loop of time.
* **Mini-Notation:** Using symbols like brackets `[ ]` to split time, asterisks `*` to multiply speed, and tildes `~` for rests to easily craft intricate drum patterns.
* **Continuous Transformation:** You can chain modifiers like `.bank()`, `.room()`, `.delay()`, and `.late()` to dynamic, evolving audio landscapes on the fly.

---

## 🚀 How to Play These Files

You don't need to install anything to hear or edit these tracks! 

1. Copy any of the `.js` or text code blocks from this repository.
2. Open your browser and go to [strudel.cc](https://strudel.cc/).
3. Paste the code into the main editor window.
4. Press **Ctrl + Enter** (or click the **Play** button) to run the code.
5. Tweak the numbers, change the samples, and make it your own!

---

## 🎼 Featured Sketches

### ⚡ Techno Driving Loop
An unrelenting, heavy electronic club loop using a four-on-the-floor 808 setup, continuous mechanical hats, and a warehouse-style reverb filter.

```javascript
setcpm(135/4)
sound(`
[-  -  oh:1 - ] [-  -  oh:1 - ] [-  -  oh:1 - ] [-  -  oh:1 oh:1],
[hh hh hh hh]   [hh hh hh hh]   [hh hh hh hh]   [hh hh hh   hh],
[-  -  -  - ]   [cp -  -  - ]   [-  -  -  - ]   [-  cp -    - ],
[bd bd bd bd]   [bd bd bd bd]   [bd bd bd bd]   [bd bd bd   bd],
[sd sd sd sd] [lt lt] * 8 hh hh 
`)
.bank("RolandTR808")
.room(.3)      // Adds a warehouse-style room reverb
.shape(.2)     // Adds analog saturation/distortion to make the 808 kick crunch
.lpf(1800)     // Low-pass filter to cut harsh high-end frequencies for a darker vibe
