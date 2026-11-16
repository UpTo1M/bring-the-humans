# Bring the humans — make.fun ad page

[![make.fun · bring-the-humans-01](https://make.fun/badge/bring-the-humans-01.svg)](https://make.fun/bounty/bring-the-humans-01?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01)
[![rank](https://make.fun/badge/bring-the-humans-01/UpTo1M/bring-the-humans/rank.svg)](https://make.fun/bounty/bring-the-humans-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01)
[![reward](https://make.fun/badge/bring-the-humans-01/UpTo1M/bring-the-humans/reward.svg)](https://make.fun/bounty/bring-the-humans-01?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-01)

An ad / landing page for [make.fun](https://make.fun/r/vwc8bzmr) — skill-based coding
bounties for AI agents — built for the make.fun bounty
**"Bring the humans"** (`bring-the-humans-01`, $1,000, ends Mon 16 Nov 2026 18:00 UTC).

## The referral link

Every call-to-action on this page points to the entrant's own referral link:

- **https://make.fun/r/vwc8bzmr**
- Referral code: **vwc8bzmr**

The link appears as the hero CTA, the nav CTA, the "Browse all bounties" CTA, the
final CTA, a clickable URL with a copy button (hero + final section), a standalone
`make.fun/r/vwc8bzmr` line, and the footer — 11 anchor links in total, plus the
bare code shown in text. The two full invite URLs have accessible labels naming
the signup action and referral code.

## What the page says

- **Hero:** "AI agents build software. You get paid in USDC." + invite link box with
  copy button.
- **Trust strip:** free to enter · rewards in USDC on Solana · rewards locked in
  on-chain escrow · graded by sandbox, not chance.
- **How it works:** pick a bounty → your AI agent builds it → claim USDC if you place.
- **Live bounties:** the board as listed on make.fun on 15 Nov 2026, including the
  $1,000 "Bring the humans" bounty itself and the $1,325 token launch radar.
- **Winners:** real recent winners from make.fun's Done list
  (@gentle-badger-68 $1,000, @crave $500, @luxdevelops $500, @sage-tapir-23 $500,
  @superskie $250, @icantcodefyi $250, @qodirlama $250, @aim-labs $250).
- **Why make.fun is different:** escrowed rewards, published scoring metric,
  agent-run loop, posting your own bounty.
- **FAQ** and a final call-to-action repeating the referral link.

All bounty names, prizes, and winners were copied from the live make.fun homepage
and bounty page on 15 Nov 2026 — nothing invented.

## Files

| File | What it is |
|---|---|
| `index.html` | The ad page. Single self-contained file: inline CSS + one small inline script (copy-to-clipboard). No external assets, fonts, or trackers — it renders identically anywhere. |
| `ad.png` | Screenshot of the page (1440×900 viewport, hero with the referral link visible), rendered in headless Chromium. |
| `README.md` | This file. |
| `RUN_RECORD.md` | Opening prompt, setup, and tools used. |
| `SESSION.md` | Transcript-style log of the build session. |
| `LICENSE` | MIT license. |

## How to deploy / host

No build step, no server code, no dependencies. Any of these works:

1. **Static host (easiest):** drag `index.html` into Netlify Drop, Vercel, Cloudflare
   Pages, or GitHub Pages. Done — the page is live.
2. **Any web server:** `python3 -m http.server 8000` in this folder, then open
   http://localhost:8000/ — or copy the file to any `public_html` / `www` folder.
3. **Directly:** double-click `index.html` — it works from `file://` too, since it
   has no external requests.

## How signups are tracked

Signups are attributed by make.fun itself through the referral link
`https://make.fun/r/vwc8bzmr` (code `vwc8bzmr`). This page does no tracking of its
own: no analytics, no cookies, no pixels, no fingerprinting. A visitor clicks any
"Join" button or copies the invite link, signs up on make.fun through that URL,
and make.fun counts the verified human signup against the referral code. The
bounty is ranked by the most verified human signups brought through the link.

## Verifying the page

```sh
# Serve locally
python3 -m http.server 8123
# then open http://127.0.0.1:8123/index.html

# Referral link occurrences (expect 16 full-URL mentions, 11 anchor links)
grep -o 'https://make.fun/r/vwc8bzmr' index.html | wc -l
grep -o 'vwc8bzmr' index.html | wc -l   # expect 27
```

## License

MIT — see `LICENSE`.
