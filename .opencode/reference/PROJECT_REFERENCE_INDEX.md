# Project Reference Index

**Project:** Simple Telegram Bot  
**Repository:** coderooz/simple-python-telegram-bot  
**Owner:** Ranit Saha (@coderooz)  
**Last Verified:** 2026-09-08  
**Verification Type:** FULL  

---

## 1. Reference Metadata

```yaml
reference:
  name: PROJECT_REFERENCE_INDEX
  version: 1.0
  status: active
  last_verified: 2026-09-08
  verification_scope: full
  project: simple-python-telegram-bot
  repository: https://github.com/coderooz/simple-python-telegram-bot
```

---

## 2. Project Identity

| Field | Value |
|-------|-------|
| **Name** | Simple Telegram Bot |
| **Type** | Telegram Bot Application |
| **Language** | Python 3.9+ |
| **Framework** | python-telegram-bot v20+ |
| **Owner** | Ranit Saha (@coderooz) |
| **License** | MIT |
| **Repository** | https://github.com/coderooz/simple-python-telegram-bot |

---

## 3. Technology Stack

| Layer | Technology |
|-------|------------|
| **Language** | Python 3.9+ |
| **Bot Framework** | python-telegram-bot >= 20.0 |
| **Package Manager** | pip |
| **CI/CD** | GitHub Actions |
| **Hosting** | Self-hosted / Cloud |

---

## 4. Root Structure

```
Telegram Bot/
├── .editorconfig              # Editor configuration
├── .github/                   # GitHub configuration
│   └── workflows/
│       └── ci.yml             # CI workflow
├── .gitignore                 # Git ignore rules
├── .opencode/                 # OpenCode configuration
│   └── reference/
│       └── PROJECT_REFERENCE_INDEX.md  # This file
├── bot.py                     # Main bot application
├── CHANGELOG.md               # Project changelog
├── CODE_OF_CONDUCT.md         # Community guidelines
├── CONTRIBUTING.md            # Contribution guidelines
├── docs/                      # Documentation
│   ├── DEVELOPERS.md          # Developer notes
│   └── telegram-web-app-notes.md  # Preserved project notes
├── .env.example               # Environment template
├── LICENSE                    # MIT License
├── README.md                  # Project readme
├── requirements.txt           # Python dependencies
└── SECURITY.md                # Security policy
```

---

## 5. Directory Reference

### `.github/`

**Type:** GitHub Configuration  
**Purpose:** Contains GitHub-specific configuration and workflows.  
**Contains:**
- `workflows/ci.yml` - CI/CD pipeline

### `.opencode/`

**Type:** OpenCode Configuration  
**Purpose:** Contains OpenCode project reference and configuration.  
**Contains:**
- `reference/PROJECT_REFERENCE_INDEX.md` - This PRI file

### `docs/`

**Type:** Documentation  
**Purpose:** Project documentation and reference materials.  
**Contains:**
- `DEVELOPERS.md` - Developer setup and contribution guide
- `telegram-web-app-notes.md` - Preserved project notes from original txt.txt

---

## 6. File Reference

### `bot.py`

**Type:** Main Application  
**Purpose:** Telegram bot application entry point.  
**Responsibility:** Handles bot initialization, command registration, and message processing.  
**Dependencies:**
- `python-telegram-bot` library
- `BOT_TOKEN` environment variable

**Key Functions:**
- `start()` - Handles `/start` command
- `help_command()` - Handles `/help` command
- `echo()` - Echoes user messages
- `main()` - Application entry point

### `requirements.txt`

**Type:** Dependency Manifest  
**Purpose:** Lists Python package dependencies.  
**Contents:**
- `python-telegram-bot>=20.0`

### `.env.example`

**Type:** Environment Template  
**Purpose:** Template for environment configuration.  
**Required Variables:**
- `BOT_TOKEN` - Telegram Bot API token

### `README.md`

**Type:** Project Documentation  
**Purpose:** Project overview, setup instructions, and usage guide.  
**Sections:**
- Features
- Setup
- Usage
- License
- Contributing
- Contact

### `CHANGELOG.md`

**Type:** Version History  
**Purpose:** Documents project changes and releases.  
**Format:** Keep a Changelog

### `SECURITY.md`

**Type:** Security Policy  
**Purpose:** Vulnerability reporting and security practices.  
**Contact:** contact@coderooz.in

### `LICENSE`

**Type:** Legal  
**Purpose:** MIT License terms.  
**Copyright:** 2024 Ranit Saha

### `CODE_OF_CONDUCT.md`

**Type:** Community  
**Purpose:** Contributor Covenant Code of Conduct v2.0.

### `CONTRIBUTING.md`

**Type:** Community  
**Purpose:** Contribution guidelines and process.

---

## 7. Application Entry Points

| Entry Point | File | Purpose |
|-------------|------|---------|
| Bot Application | `bot.py` | Main bot startup and command handling |
| Environment Config | `.env` | Bot token and configuration |
| Dependencies | `requirements.txt` | Python package list |

---

## 8. Scripts & Commands

### Development

```bash
# Install dependencies
pip install -r requirements.txt

# Run the bot
python bot.py

# Run with environment variable
BOT_TOKEN=your_token python bot.py
```

### Testing

```bash
# Check Python syntax
python -m py_compile bot.py

# Lint with flake8
flake8 bot.py
```

### CI/CD

```bash
# Triggered automatically on push/PR to main/master
# Runs: lint, syntax check, multi-version Python testing
```

---

## 9. Configuration

### Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| `BOT_TOKEN` | Yes | Telegram Bot API token from @BotFather |

### Editor Configuration

**File:** `.editorconfig`  
**Settings:**
- Indent: 4 spaces (Python)
- Line endings: LF
- Charset: UTF-8
- Trim trailing whitespace: Yes
- Insert final newline: Yes

---

## 10. Documentation

| Document | Location | Purpose |
|----------|----------|---------|
| README | `README.md` | Project overview and setup |
| Developer Notes | `docs/DEVELOPERS.md` | Development guide |
| Changelog | `CHANGELOG.md` | Version history |
| Security | `SECURITY.md` | Security policy |
| License | `LICENSE` | MIT License |
| Contributing | `CONTRIBUTING.md` | Contribution guidelines |
| Code of Conduct | `CODE_OF_CONDUCT.md` | Community standards |
| Web App Notes | `docs/telegram-web-app-notes.md` | Preserved project notes |

---

## 11. Architectural Relationships

```
bot.py
    │
    ├── CommandHandler("start", start)
    ├── CommandHandler("help", help_command)
    └── MessageHandler(filters.TEXT & ~filters.COMMAND, echo)
            │
            └── python-telegram-bot library
                    │
                    └── Telegram Bot API
```

---

## 12. Project-Specific Conventions

- **Async/Await:** All handler functions are async
- **Environment Variables:** Sensitive data stored in `.env`
- **Documentation:** All docs in `docs/` directory
- **CI:** GitHub Actions for automated testing
- **Code Style:** PEP 8 compliant

---

## 13. Known Structural Constraints

- Bot token must be kept secret (never committed)
- python-telegram-bot v20+ requires Python 3.9+
- Single-file bot architecture (all logic in `bot.py`)
- Polling-based (not webhook)

---

## 14. Reference Maintenance Log

### 2026-09-08

**Change:** Initial PRI creation  
**Classification:** ADDED  
**Updated:**
- Created complete project reference index
- Documented all files and directories
- Mapped architectural relationships
- Verified against actual repository

**Verification:** FULL

---

## 15. Future Considerations

- **Web Interface:** Notes preserved in `docs/telegram-web-app-notes.md`
- **Additional Commands:** Can be added to `bot.py`
- **Webhook Support:** Could replace polling for production
- **Database Integration:** For persistent data storage
- **Multi-bot Support:** Architecture could be extended

---

*This PRI is maintained as part of the project's governance compliance. Update whenever structural changes occur.*
