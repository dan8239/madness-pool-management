# Madness Pool Management

## Overview
March Madness bracket pool and side-bet management for Dan's annual pool (~300+ entries).

## Key Spreadsheets

### Betting Pool (side bets between friends)
- **Sheet:** `14aU8B6VVN9_8yZPflwNKti2u7oHUws29l6iVc8XH5w0`
- **Tab:** `All Bets` — one row per wager, frozen ledger at top
- **Use `/bet` command** for quick bet operations

### Payments Tracker (bracket pool buy-ins & payouts)
- **Sheet:** `1w-K1_DhYvievrvfeCBCKtgZszETG66bsbhlwY4N11I8`
- Tabs by year (2017-2025), each with: Player, Total Payment, Paid Machi, Paid Dan, Alias, Acquaintance
- Dan and Machi co-manage the pool — each collects from their half of players
- $25 per bracket entry, players can have multiple entries (Name, Name 2, Name 3)

## CBS Sports Bracket Pool
- Pool standings URL: `https://picks.cbssports.com/college-basketball/ncaa-tournament/bracket/pools/kbxw63b2ge2daojrge2do===/standings`
- Pool ID: `kbxw63b2ge2daojrge2do===`
- 300+ bracket entries per year

## People
- **Dan (Daniel Pfeiffer)** — co-manager, "me" in conversations
- **Machi (Kevin Maciejewski)** — co-manager
- **Markert (Brian Markert)** — bettor, friend
- **Doerr (Kevin Doerr)** — bettor, friend

## MCP Tools
- Google Sheets access via `mcp-google-sheets` (user-scoped, OAuth configured)

## Conventions
- Keep sheets human-readable — friends need to read them too
- Use TRUE/FALSE for booleans in sheets
- Winner column uses "Fav" / "Dog" not team names
