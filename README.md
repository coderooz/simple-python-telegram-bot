# Simple Telegram Bot

A Telegram bot built with Python and the `python-telegram-bot` library (v20+).

[![CI](https://github.com/coderooz/simple-python-telegram-bot/actions/workflows/ci.yml/badge.svg)](https://github.com/coderooz/simple-python-telegram-bot/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

## Features

- Responds to `/start` command with a greeting message
- Responds to `/help` command with usage instructions
- Echoes any text message sent to it
- Environment variable support for bot token
- Async/await architecture (python-telegram-bot v20+)

## Setup

### Prerequisites

- Python 3.9 or higher
- A Telegram Bot Token (from [@BotFather](https://t.me/BotFather))

### Installation

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

## Usage

1. Start the bot with `python bot.py`
2. Open Telegram and find your bot
3. Send `/start` to get a greeting
4. Send `/help` for usage information
5. Send any text message to have it echoed back

## Development

See [docs/DEVELOPERS.md](docs/DEVELOPERS.md) for:
- Development setup
- Code structure
- Adding new commands
- Testing guidelines
- Deployment instructions

## Project Structure

```
Telegram Bot/
├── bot.py              # Main bot application
├── requirements.txt    # Python dependencies
├── .env.example        # Environment template
├── docs/               # Documentation
│   ├── DEVELOPERS.md   # Developer notes
│   └── telegram-web-app-notes.md
├── .github/workflows/  # CI/CD
│   └── ci.yml
└── .opencode/          # Project reference
    └── reference/
        └── PROJECT_REFERENCE_INDEX.md
```

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## Security

For security concerns, please see [SECURITY.md](SECURITY.md) or contact contact@coderooz.in.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes.

## Contact

Created by [Ranit Saha](https://github.com/coderooz).

- GitHub: [@coderooz](https://github.com/coderooz)
- Email: contact@coderooz.in
