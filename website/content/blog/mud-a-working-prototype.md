---
title: "Mud a Working Prototype"
date: 2020-08-11T17:04:44Z
draft: false
---

---

[Server](https://github.com/Moppler/TextAdventure-Server)
|
[Client](https://github.com/Moppler/TextAdventure-Client)

---

After quite a lot of experimenting as well as playing around with different
methods of communication between the client and the server, I finally settled on
something that seems to work.

Server asks: What would you like to do? and provides choices.

```javascript
{
  type: 'requestInstruction',
  data: {
    availableInstructions: [
      { name: 'Look', instruction: 'look' },
      {
        name: 'Move',
        instruction: 'move',
        arguments: [
      	  {
            type: 'select',
            name: 'direction',
            playerPrompt: "Which Direction?",
            options: [
            	{ name: 'North', value: 'north' },
          		{ name: 'East', value: 'east' },
            ],
          },
      	],
      },
    ],
  },
}
```

The client responds with an instruction based on the players selection.

If the instruction requires no additional information, the server will provide
display information and then a new `requestInstruction`

```javascript
// Client -> Server
{
  type: 'issueInstruction',
  data: {
    instructionType: 'look',
  }
}

// Server -> Client
{
  type: 'render',
  data: {
    message: 'A description of the room you are in...',
  }
}
```

Some instructions require additional information in the form of arguments. These
are supplied to the player with the `requestInstruction` message and can be
quite complex with a select option. They can also be simple with freetext input.

The goal of this structure is to leave the client in control of how the player
should interact with this information and instead only provide the tools to play
the game. It should be possible to construct a very simple client using this
structure, while leaving it open to improvements in the future.
