# Brand System Template — first-time user flow

**Category:** 99-uncategorized
**Source:** brand-system-template.md
**Generated:** 2026-08-28

## Overview

This repository contains a generalized AI agent skill ready for use with Claude Code, Hermes Agent, or any PAL-compliant agent framework.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/diamitani/brand_system_template-skill.git
   ```

2. Import the skill into your agent framework:
   ```bash
   # For Claude Code
   @skill SKILL.md
   
   # For Hermes Agent
   skill_view(name='brand_system_template')
   ```

## Configuration

This skill uses placeholder values for company-specific data:
- `{COMPANY_NAME}` — Replace with your company name
- `{COMPANY_SLUG}` — Replace with your company URL slug
- `{USER_HOME}` — Replace with the user's home directory
- `{USER_NAME}` — Replace with user's name

## License

MIT License — See LICENSE file for details.

## Support

Questions? Open an issue on GitHub.
