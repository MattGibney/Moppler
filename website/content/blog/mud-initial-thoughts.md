---
title: "MUD Initial Thoughts"
date: 2020-08-07T22:57:38Z
draft: false
---

### A little history

This isn't the first time i've had a go at building MUDs. I've tried a couple of
different times over the years. I've tried building from scratch and i've tried
using frameworks. All of them have worked with limited success but none of them
have been totally successful. In hindsight, I think i've struggled to get
excited about them because they have all felt awkward to program. A combination
of using telnet and trying to emulate things i've seen in existing populat MUDs
have muddied my views of things. With this latest attempt I want to try and fix
my issues.

### Clients

In my opinion, telnet has served its purpose and is not worth pursuing anymore;
Time to move on. After a lot of thought I have settled on shipping a client.
I'd be interested in making use of ssh for this [theres a great blog post about it.](https://medium.com/@shazow/ssh-how-does-it-even-9e43586e4ffc)

In order to keep things simple and allow me to iterate quickly, the plan is to
start with a CLI written in Node and shipped via NPM. It's free, easy and I
know exactly how to do it. Making use of the terminal provides me with a strict
limitation on aesthetics, keeping my focus on mechanics. The best part however,
is that my implementation makes it pretty easy to add different, more
sophisticated, clients in the future.

#### Code

[Server](https://github.com/Moppler/TextAdventure-Server)

[Client](https://github.com/Moppler/TextAdventure-Client)