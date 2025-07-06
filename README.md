# Discord Bot

A feature-rich Discord bot built with Python using the discord.py library. This bot includes moderation features, role management, polls, and various utility commands.

## Features

### 🤖 Core Commands

- **!hello** - Greets the user with a mention
- **!reply** - Demonstrates reply functionality
- **!dm** - Sends a direct message to the user with their input
- **!poll** - Creates a poll with thumbs up/down reactions

### 🛡️ Moderation

- **Auto-moderation** - Automatically deletes messages containing profanity
- **Content filtering** - Warns users when inappropriate language is used

### 👥 Role Management

- **!assign** - Assigns the "Gamer" role to the user
- **!remove** - Removes the "Gamer" role from the user
- **!secret** - Exclusive command for users with the "Gamer" role

### 🎉 Welcome System

- **Auto-welcome** - Sends a direct message to new server members

## Setup

### Prerequisites

- Python 3.8 or higher
- A Discord bot token
- Discord server with appropriate permissions

### Installation

1. Clone this repository:

   ```bash
   git clone <repository-url>
   cd discordbot
   ```

2. Install required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the root directory:

   ```env
   DISCORD_TOKEN=your_bot_token_here
   ```

4. Make sure your bot has the following permissions in your Discord server:
   - Send Messages
   - Manage Messages (for moderation)
   - Manage Roles (for role assignment)
   - Add Reactions (for polls)
   - Read Message History

### Running the Bot

```bash
python main.py
```

## Configuration

### Environment Variables

- `DISCORD_TOKEN` - Your Discord bot token (required)

### Bot Settings

- **Command Prefix**: `!` (can be changed in `main.py`)
- **Secret Role**: "Gamer" (can be modified in the `secret_role` variable)

## Commands Reference

| Command            | Description                   | Usage                                | Permissions     |
| ------------------ | ----------------------------- | ------------------------------------ | --------------- |
| `!hello`           | Greets the user               | `!hello`                             | Everyone        |
| `!assign`          | Assigns the Gamer role        | `!assign`                            | Everyone        |
| `!remove`          | Removes the Gamer role        | `!remove`                            | Everyone        |
| `!dm <message>`    | Sends a DM to the user        | `!dm Hello there!`                   | Everyone        |
| `!reply`           | Replies to the user's message | `!reply`                             | Everyone        |
| `!poll <question>` | Creates a poll                | `!poll Should we add more features?` | Everyone        |
| `!secret`          | Secret command                | `!secret`                            | Gamer role only |

## File Structure

```
discordbot/
├── main.py          # Main bot file with all commands and events
├── requirements.txt # Python dependencies
├── .env            # Environment variables (not in repo)
├── discord.log     # Bot logging file (generated)
└── README.md       # This file
```

## Logging

The bot creates a `discord.log` file that contains detailed logging information for debugging and monitoring purposes.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you encounter any issues or have questions, please open an issue on the repository.

## Disclaimer

This bot is for educational purposes. Make sure to comply with Discord's Terms of Service and Community Guidelines when using and hosting bots.
