# 🤖 BoardHub

BoardHub is a Discord bot for playing board games with your friends.

At the moment, the bot includes **ito**. More games will be added over time.

## 👨‍💻 Installation

If you don't have a Python or Docker environment, you can invite the hosted version of the bot using [this link](https://discord.com/oauth2/authorize?client_id=1520256776392409230&permissions=563224861984832&integration_type=0&scope=bot).



⚠️ **Notice**

This bot is operated as a personal project.

Performance may slow down if the number of users grows significantly. The hosted bot may also be shut down at any time without prior notice.

If you need long-term availability or guaranteed uptime, consider hosting your own instance.

### Requirements

- Python (>= 3.10)
  - uv
- Docker

### Python

```bash
$ uv sync
$ uv run python main.py
```

### Docker

```bash
$ docker build .
$ docker compose up
```

## 🎮 Supported Games

### ito

**ito** is a cooperative party game where players work together to arrange hidden number cards from lowest to highest.

Each player receives a number between 0 and 100, but they are not allowed to reveal it directly. Instead, players use examples based on a shared topic to express how large or small their number feels.

#### Commands

- **`/ito create`**
  - Creates a game.

- **`/ito join`**
  - Joins the game.

- **`/ito leave`**
  - Leaves the game.

- **`/ito state`**
  - Shows the current participants.

- **`/ito start [topic]`**
  - Starts a game.
  - `topic` is optional.
  - If specified, the game starts with that topic.
  - If omitted, a random topic is selected.
  - Each participant receives their number card via DM.

- **`/ito open-cards`**
  - Reveals all number cards.

- **`/ito end`**
  - Ends the current game.

- **`/ito kick @user`**
  - Removes the specified player from the game.

- **`/ito help`**
  - Displays the command list.

#### How to Play

1. Create a game with `/ito create`.
2. Players join with `/ito join`.
3. Start the game with `/ito start`.
4. Check your number card and the topic in your DM.
5. Discuss the topic and try to determine the correct order of all cards.
6. Reveal the cards using `/ito open-cards`.
7. Start another round with `/ito start`, or finish the session with `/ito end`.

#### Topics

The bot includes a collection of built-in topics.

If no topic is specified when starting a game, one will be selected at random.

You can also provide your own topic using `/ito start [topic]`.

##### Example Topics

```text
/ito start Places you'd like to visit
/ito start Foods that go well with rice
/ito start Requests that would make even a god uncomfortable
```

##### Notes

- Some topics are generated with AI.
- AI-generated topics may vary in quality and difficulty.

## 📨 Contact

For bug reports, feature requests, or other inquiries, please contact [terry (@terrytwitch)](https://x.com/terrytwitch).
