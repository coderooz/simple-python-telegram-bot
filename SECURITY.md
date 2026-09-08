# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability within this project, please send an email to contact@coderooz.in. All security vulnerabilities will be promptly addressed.

**Please do NOT report security vulnerabilities through public GitHub issues.**

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.1.x   | :white_check_mark: |
| < 1.1   | :x:                |

## Security Measures

- Bot tokens are stored in environment variables, never hardcoded
- `.env` files are excluded from version control via `.gitignore`
- Dependencies are pinned to known versions
- GitHub Actions CI includes security checks

## Best Practices

When deploying this bot:

1. **Never commit your bot token** to version control
2. **Use environment variables** for sensitive configuration
3. **Keep dependencies updated** regularly
4. **Run the bot with minimal permissions** required
5. **Monitor bot activity** for unusual behavior

## Dependency Security

This project uses `python-telegram-bot` which is actively maintained and security-patched. Run `pip audit` regularly to check for known vulnerabilities.

## Contact

For any security concerns, please contact:
- Email: contact@coderooz.in
- GitHub: [@coderooz](https://github.com/coderooz)
