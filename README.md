# Boring Party Bingo

Boring Party Bingo is a casual social game designed to be played during real-life conversations.

Imagine being at a party, meetup, or dinner where people are deeply engaged in a topic.
Sometimes it is unfamiliar or exhausting.
Sometimes everyone is genuinely interested and fully involved.
Either way, the conversation keeps circling around the same words, phrases, and ideas.

Instead of checking your phone, you start noticing patterns.
And you turn them into a game.

---

## How the Idea Started

The idea came from a real situation.

After losing our jobs in tech, a close friend and I were emotionally burned out.
Tech-related conversations felt heavy and unavoidable.
At a small party, the same topics and buzzwords kept appearing again and again.

At some point, my friend started drawing a bingo board on paper.
Each cell contained a word that kept coming up in the conversation.
Every time someone said one of them, we marked it.

Listening became playful.
Soon, others joined in.

---

## The Idea

Party Bingo is a game that lives **on top of a real conversation**.

You play it while people are talking.

- at a party
- during a meetup
- at dinner
- or any group conversation

The game can be used in different ways:

- **Solo**, when the topic is not for you, but you are still present
- **Together**, when the whole group is engaged and plays along

The conversation is not interrupted.
It becomes the game engine.

---

## Game Modes

### Solo
- Single player mode
- Uses the same room-based game model as multiplayer
- No dependency on other players

### Room (Multiplayer)
- Multiple players join the same room
- Game events are synchronized via WebSocket
- When one player wins, the result is broadcast to all participants

---

## Principles and Constraints

- No user accounts or authentication
- Players are temporary entities
- Game rooms have a limited lifetime
- Temporary disconnections are allowed
- Server state can be restored within a short time window

These constraints are intentional and directly influence the system architecture.

---

## Planned Technology Stack

### Backend
- Node.js
- NestJS
- WebSocket (Socket.IO)
- In-memory state with Redis as temporary persistence (TTL)
- Docker

### Frontend
- React
- Progressive Web App (PWA)
- WebSocket client

---

## Architectural Approach

- Game logic and game state are separated from the WebSocket communication layer
- The same room-based model is used for both solo and multiplayer modes
- The system is designed to tolerate short network interruptions

The project is developed incrementally, starting from a minimal working foundation.

---

## Status

Work in progress.

---

## License

MIT


