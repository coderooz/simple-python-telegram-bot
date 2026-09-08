# Developer Notes

This document provides guidance for developers working on the Simple Telegram Bot project.

## Project Overview

A Telegram bot built with Python and the `python-telegram-bot` library (v20+). The bot responds to commands and echoes messages.

## Development Setup

### Prerequisites

- Python 3.9 or higher
- pip (Python package manager)
- A Telegram Bot Token (from [@BotFather](https://t.me/BotFather))

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/coderooz/simple-python-telegram-bot.git
   cd simple-python-telegram-bot
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment**
   ```bash
   cp .env.example .env
   # Edit .env and add your BOT_TOKEN
   ```

5. **Run the bot**
   ```bash
   python bot.py
   ```

## Code Structure

```
Telegram Bot/
├── bot.py              # Main bot application
├── requirements.txt    # Python dependencies
├── .env.example        # Environment template
├── docs/               # Documentation
│   ├── DEVELOPERS.md   # This file
│   └── telegram-web-app-notes.md
└── .github/workflows/  # CI/CD
    └── ci.yml
```

## Code Style

- Follow PEP 8 Python style guidelines
- Use async/await for all handler functions
- Keep functions small and focused
- Add docstrings to all functions
- Use meaningful variable names

## Adding New Commands

1. Create an async handler function:
   ```python
   async def my_command(update: Update, context: ContextTypes.DEFAULT_TYPE) -> None:
       """Handle /mycommand."""
       await update.message.reply_text('Response here')
   ```

2. Register the handler in `main()`:
   ```bash
   application.add_handler(CommandHandler("mycommand", my_command))
   ```

## Testing

### Manual Testing

1. Start the bot locally
2. Open Telegram and find your bot
3. Test all commands:
   - `/start` - Should greet the user
   - `/help` - Should show usage info
   - Send any text - Should echo back

### Automated Testing

The CI pipeline runs:
- Python syntax checks
- Linting with flake8
- Multi-version Python testing

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `BOT_TOKEN` | Yes | Telegram Bot API token from @BotFather |

## Common Issues

### Bot doesn't respond

1. Verify `BOT_TOKEN` is set correctly
2. Check bot is running without errors
3. Ensure you're messaging the correct bot

### Import errors

1. Ensure virtual environment is activated
2. Run `pip install -r requirements.txt`
3. Check Python version (3.9+)

### Rate limiting

Telegram has rate limits. If you hit them:
- The library handles retries automatically
- Add delays between messages if needed
- Check [Telegram Bot API limits](https://core.telegram.org/bots/faq#broadcasting-to-users)

## Deployment

### Environment Variables

Set `BOT_TOKEN` in your deployment environment:
- **Heroku**: Settings → Config Vars
- **Railway**: Variables tab
- **Vercel**: Settings → Environment Variables
- **Docker**: Use `.env` file or environment

### Running as a Service

Use a process manager like `systemd` or `supervisor` to keep the bot running:

```ini
# /etc/supervisor/conf.d/telegram-bot.conf
[program:telegram-bot]
command=/path/to/venv/bin/python /path/to/bot.py
directory=/path/to/project
autostart=true
autorestart=true
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run linting: `flake8 .`
5. Test your changes
6. Submit a pull request

## Resources

- [python-telegram-bot Documentation](://docs.python-telegram-bot.org/)
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [BotFather Commands](https://core.telegram.org/bots#creating-a-new-bot)

## Contact

- **Author**: Ranit Saha
- **GitHub**: [@coderooz](https://github.com/coderooz)
- **Email**: contact@coderooz.in
