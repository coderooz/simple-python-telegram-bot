# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2026-09-08

### Changed
- Updated `python-telegram-bot` from v13.7 to v20+
- Modernized bot code to use `Application` class instead of `Updater`
- Converted handler functions to async/await pattern
- Added environment variable support for bot token

### Added
- `.env.example` for environment configuration
- `.gitignore` for Python projects
- `SECURITY.md` security policy
- `CHANGELOG.md` this file
- `docs/DEVELOPERS.md` developer documentation
- `docs/telegram-web-app-notes.md` preserved project notes
- `.github/workflows/ci.yml` GitHub Actions CI workflow
- `.opencode/reference/PROJECT_REFERENCE_INDEX.md` Project Reference Index

### Removed
- Removed hardcoded bot token (now uses environment variable)

## [1.0.0] - 2024-01-01

### Added
- Initial release
- Basic bot with `/start`, `/help` commands
- Echo functionality for text messages
- Python Telegram Bot v13.7 implementation
