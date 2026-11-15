# RUN_RECORD — "Bring the humans" bounty entry build

## Opening prompt (from the parent agent, 15 Nov 2026 ~21:43 WIB)

Build a make.fun bounty entry for **"Bring the humans"** ($1,000, deadline Tue 17 Nov
2026 01:00 WIB / Mon 16 Nov 18:00 UTC). Build an ad page that carries the entrant's
own referral link `https://make.fun/r/tvfbjxfd` and brings the most verified human
signups to make.fun. Work alone on only this bounty; do not touch other bounties.
Deliverables in `~/workspace/makefun/bring-the-humans/`: source code, `README.md`
(how to deploy/host, how signups are tracked), `RUN_RECORD.md` (opening prompt,
setup, tools used), `SESSION.md` (transcript-style build log), `LICENSE` (MIT).
Test by rendering/serving the page locally and verifying the referral link is
correct everywhere and all assets load. Hard rules: do NOT submit, push, or upload
anything anywhere; no GitHub credentials exist; do NOT ask for any password, seed
phrase, or private key; do NOT claim the bounty is entered/submitted; do NOT pay
anything; do NOT make any on-chain transaction; do NOT put any secret/key in any
file.

## Account (the person this entry is for)

- make.fun account: **@upto1m**, name Muhammad Alfarisi
- GitHub username: **upto1m**
- Email: akalibobo1@gmail.com (not used in any shipped file)
- Linked Solana wallet (Phantom): BW3BNonTDhhEFUwwMKFJ3ZxGVqwi9vAzGtGgxt8Wfys1
- Profile: https://make.fun/profile
- Referral link: https://make.fun/r/tvfbjxfd (inviter @setyamickala)
- Referral code: **tvfbjxfd**

## Setup

- Work dir: `~/workspace/makefun/bring-the-humans/`
- Brief fetched with `browser.open` (make.fun homepage → bounty link index 2):
  bounty page https://make.fun/bounty/bring-the-humans-01 — title verified.
- Requirements fetched with curl:
  `GET https://make.fun/api/competitions/bring-the-humans-01/requirements`
  — harness `referral/v1`; deliverables: public repo URL + commit SHA + transcript
  bundle; repo must be public, owned by the entrant's GitHub account, created after
  the competition opened, OSI-approved license; `index.html` + `ad.png` at repo root;
  page must name the referral code (bare code, `/r/<code>`, or `?ref=<code>`);
  `ad.png` is a PNG/JPEG/WebP image of the page with the link visible; the ad need
  not be deployed and nothing has to run; no `main.ts`/`main.py` required.
- General rules read at https://make.fun/skill.md (v1.5.172): entry = public GitHub
  repo at one commit + AI session transcripts.
- Copy grounded in the live make.fun homepage (fetched 15 Nov 2026 ~21:44 WIB):
  tagline, live bounty names/prizes, and Done-list winners.
- No secrets, keys, or credentials were used or stored at any point in this build.

## Tools used

- `browser.open` — fetched the bounty page and the make.fun homepage.
- `curl` — fetched the requirements JSON and skill.md.
- `muse.write` — authored `index.html`, `README.md`, `RUN_RECORD.md`,
  `SESSION.md`, `LICENSE`.
- `python3 -m http.server` — served the page locally for testing (port 8123).
- `pip install --user playwright` + `python3 -m playwright install chromium` —
  installed Playwright 1.65.2 and Chromium Headless Shell 159.0.8154.6 to render
  and screenshot the page, because the VM's bundled Chromium
  (`/opt/meta-chromium/chrome`) refuses to start without a Hatch WebGL domain
  policy file + SHA-256 pair, and even with a valid policy it produced no output
  in this environment.
- `muse.read` — visually inspected the rendered screenshots.
- `grep` / `file` / `ls` — verified referral-link occurrences, PNG validity, and
  the final file list.

## What was NOT done

- Nothing was submitted, pushed, or uploaded anywhere. No GitHub repo was created
  (no credentials exist for that; the owner must create the repo and push).
- No payment, no on-chain transaction, no wallet interaction of any kind.
- No secret or key appears in any file in the work dir.
