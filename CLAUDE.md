# Madness Pool Management

## Overview
March Madness bracket pool and side-bet management for Dan's annual pool (~238 entries in 2026).

## Key Spreadsheets

### Betting Pool (side bets between friends)
- **Sheet:** `14aU8B6VVN9_8yZPflwNKti2u7oHUws29l6iVc8XH5w0`
- **Tab:** `All Bets` (sheet ID `1832942550`)
- Rows 1-11: Frozen ledger + header. Row 12: data header. Row 13+: bets.
- **Use `/bet` command** for quick bet operations

### Payments Tracker (bracket pool buy-ins & payouts)
- **Sheet:** `1w-K1_DhYvievrvfeCBCKtgZszETG66bsbhlwY4N11I8`
- **2026 tab** (sheet ID `314861584`): Rows 1-7 payouts, 9-10 stats, 11 header (frozen), 12-249 entries, 250 TOTAL
- Columns: Player | Total Payment | Paid Machi | Paid Dan | Alias | Acquaintance | Champion
- $25 per bracket entry. Paid columns hold actual amount received (usually 25, sometimes less).
- Alias/Acquaintance formulas use REGEXREPLACE to strip CBS 6-char suffixes + " 2"/" 3" patterns, then VLOOKUP against ACQUAINTANCES tab

## CBS Sports Bracket Pool
- Pool standings URL: `https://picks.cbssports.com/college-basketball/ncaa-tournament/bracket/pools/kbxw63b2ge2daojrge2do===/standings`
- Requires login (use Playwright MCP). Page is JS-rendered, needs pagination (25 per page).
- 2026 bracket names have random 6-char alphanumeric suffixes (e.g. "Bradley Baker DKhieq")

## People
- **Dan (Daniel Pfeiffer)** — co-manager, "me"/"I" in conversations
- **Machi (Kevin Maciejewski)** — co-manager, collects from his half
- **Markert (Brian Markert)** — bettor, friend
- **Doerr (Kevin Doerr)** — bettor, friend

## MCP Tools
- `mcp-google-sheets` — sheet reads/writes (user-scoped, OAuth configured)
- `@playwright/mcp` — browser automation for CBS scraping, Venmo, ESPN scores

## Conventions
- Keep sheets human-readable — friends need to read them too
- Use TRUE/FALSE for booleans in sheets
- Winner column uses "Fav" / "Dog" not team names
- Paid columns hold actual dollar amount received, not just TRUE/FALSE
- Bets come via voice input — expect casual/ambiguous language, always confirm before writing
- Same game can have multiple bet rows (different bettors on each)
- ESPN scoreboard for final scores: `https://www.espn.com/mens-college-basketball/scoreboard/_/date/YYYYMMDD/group/100`
