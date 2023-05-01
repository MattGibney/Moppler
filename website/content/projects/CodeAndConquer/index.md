---
Title: Code and Conquer
type: projects
thumbnail: thumbnail.jpg
summary: RTS for programmers
---

## Code and Conquer

---

Status: **Prototyping** | [Source Code](https://github.com/Moppler/CodeAndConquer)

---

Code and Conquer is a real-time strategy game where you control your units by
writing code. The game is currently in the early stages of development. It's
loosely based on the classic game [Command and Conquer: Generals](https://en.wikipedia.org/wiki/Command_%26_Conquer:_Generals) by EA Games.

The main goal is to create a game that is incredibly flexible. The idea is that
the server provides the absolute bare minimum of functionality and the players
are responsible for everything else. This means that the game can be played
however the players want. The server will provide the tools and the players will
use them to create AIs to play the game for them.

Players issue commands via a REST API. These commands are queued upo and
processed by the server each game tick. Commands are run in the order that they
are received, so players have an advantage by writing efficient code. There is a
real risk that Latency would have a major impact of player however, game servers
will have their location publicly available and players can always choose to
run their code on VPSs in the same location as the server.

### Why?

I'm a huge fan of the game Screeps. It's a game where you control your units by
writing JavaScript. I love the idea of the game but I don't like the execution.
Game play is slow as each server tick takes several seconds to process. In
addition, all code runs on the game servers. This means that players have no
control over the environment that their code runs in. On top of that, there
are major limitations to what is possible, especially when it comes to tracking
state across ticks.

Whenever I play Screeps, I find myself wishing that I could instantiate classes
and have them persist across ticks. I also wish that I could run my code on my
own servers so that I could have more control over the environment. I appreciate
that this would be a nightmare to manage and would be open to abuse, but I still
wish that it was possible. I also appreciate that this is entirely a me problem,
there are some incredible coders out there that have written amazingly complex
AIs for Screeps. I'm just not one of them.

I was a huge fam of Command and Conquer: Generals when I was younger. I loved
the idea of controlling an army and building a base. I'm not sure of exactly how
many hours I spent playing it, but it was a lot. In my opinion, it an incredibly
well balanced game. It's clear that a lot of time and effort went into making
sure that each faction was balanced against the others. I also loved the
campaigns. I'm a huge fan of the story and the characters. I've always been a
fan of the Command and Conquer series and I think that Generals is the best of
them.

I wanted to create a game experience like Screeps but with the game play of
Command and Conquer. I think the two would work really well together and provide
a lot of room for fun and interesting game play. I also think that it would be
an interesting challenge to create a game that is so flexible. I'm not sure how
well it will work, but I'm excited to find out.

### Game Play

The game is played in real time. Game ticks are processed as quickly as possible
ideally as soon as all players have issued commands or after a set number of
seconds. Players issue commands via a REST API, the approach for issuing these
commands is up to the player. They are expected to write code in a language of
their choice and host it somewhere.

Games are expected to be quick. If communication between players and the server
is quick, ticks can be processed much faster than a human could keep up with. It
is expected that games run for a few minutes at most. This means that players
will need to write code that is efficient and can run quickly. It also means
that players will be able to test their code quickly.

After each game, a replay will be available. This will show the commands that
each player issued and the results of those commands. This will allow players to
see how their code performed and where it could be improved. It also means that
players can see how their opponents issue commands and learn from them. The best
part of this is that the source code is still private to the player.
