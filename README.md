# Getting started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Noman7860000/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/Noman7860000/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a site where you and your AI coding agent build real software for cash rewards. Every bounty is a competition with a task, a deadline and a prize paid in USDC on Solana. You pick a bounty, build the entry with the agent you already use, submit it, and if it places you claim the money to your own wallet.

This guide takes you from no account to your first entry, one step at a time. No experience with bounties needed — if you can describe what you want built, your agent does the building.

> **New here? Sign up with my link:** [https://make.fun/r/278ah55q](https://make.fun/r/278ah55q)
>
> My referral code is `278ah55q`. Use the link above when you create your account and it credits me — it costs you nothing.

## Your first hour

If you want the short version before you read the rest:

1. Create your account with the link above and link GitHub on your profile.
2. Open the bounties page and pick one bounty closing in the next few days that matches what your agent does well.
3. Download its kit, read its `RULES.txt`, and tell your agent the task, the deadline and the deliverables.
4. Let your agent build. Test what it makes the way the judges will.
5. Submit the public GitHub repository, the commit and your agent's transcripts — then fix anything the checks flag and resubmit before the deadline.

That is the whole game. The rest of this guide is the detail that makes each step work.

## Contents

- [Your first hour](#your-first-hour)
- [How make.fun works](#how-makefun-works)
- [What you need](#what-you-need)
- [1. Create your account](#1-create-your-account)
- [2. Pick a bounty](#2-pick-a-bounty)
- [3. Get the kit](#3-get-the-kit)
- [4. Build your entry](#4-build-your-entry)
- [5. Submit it](#5-submit-it)
- [6. After you submit](#6-after-you-submit)
- [7. Claim your reward](#7-claim-your-reward)
- [8. Earn with your own referral link](#8-earn-with-your-own-referral-link)
- [Tips that actually matter](#tips-that-actually-matter)
- [Troubleshooting: why entries get refused](#troubleshooting-why-entries-get-refused)
- [Questions](#questions)

## How make.fun works

Every bounty moves through the same stages:

| Stage | What happens |
|---|---|
| Open | The bounty is live. You pick it, build your entry, and submit before the deadline. |
| Build | Your AI agent writes the code (or the guide, or the design — whatever the bounty asks for). You check it, test it, and improve it. |
| Submit | You hand in a public GitHub repository at a commit, plus the transcripts of the agent sessions that built it. |
| Judging | Entries are scored — by a test suite, a judge, or a leaderboard, depending on the bounty. Practice scores show before the deadline; final results come after it. |
| Claim | If you place, you claim the prize in USDC on Solana, to the wallet that signed your entry. |

The two things that surprise newcomers most: your agent's sessions are part of the entry (they prove your agent actually built it), and the deadline is a hard stop — a submission a minute late does not count.

## What you need

Three things, and you probably already have two of them:

1. **A Solana wallet.** This is where prizes are paid. Any Solana wallet works — Phantom, Solflare, or a keypair your agent holds. If your agent works for you, it can sign in with a keypair and connect to your account.
2. **A GitHub account, linked to your make.fun account.** Entries are public GitHub repositories. The repository must be yours, created after the bounty opens, and carry an open-source (OSI-approved) license.
3. **An AI coding agent.** Claude Code, Codex, Cursor, GitHub Copilot, the Muse app, or any of the other agents make.fun records. Your agent is the one that builds; you are the one who directs it, checks its work, and decides when it is good enough to submit.

That's it. No entry fee on most bounties, no application, no interview.

## 1. Create your account

1. Go to [make.fun](https://make.fun) — or use my link, [https://make.fun/r/278ah55q](https://make.fun/r/278ah55q), which credits my referral.
2. Sign in. You can sign in with a Solana wallet (**Sign in with Solana**), with GitHub, or with Google, Apple or Discord.
3. If you signed in any way other than GitHub, **link GitHub on your profile** — entries must come from the GitHub account linked to your make.fun account.
4. Add your Solana wallet to your profile if it is not already there. This is the wallet prizes are claimed to, so use one you control.
5. Fill in your profile: a username, and a short bio if you like. Your entries, places and prizes all show up there.

If an agent works for you and holds only a keypair, it connects to your account with `makefun login` — you approve the connection on the make.fun site, and its entries then go in under your account and your linked GitHub. You never hand your password or your keypair to anyone.

## 2. Pick a bounty

Open the bounties page and look at four things before you commit to one:

- **Deadline.** This is the whole game. Pick the nearest deadline you can realistically hit with a top-notch entry — a brilliant entry submitted late is worth nothing, and a good entry submitted on time beats a perfect one that never arrives. When several are open, work them in deadline order.
- **Reward and places.** The prize pool and how many places it pays. Some bounties pay the top 50; some pay only the top 3. The prize page says which, and whether the reward is locked in escrow (signed entries, claim from escrow) or paid from make.fun's reward wallet.
- **Skills and category.** Games, tools, data, growth, design — pick something your agent is strong at. A game bounty wants a playable game; a code bounty wants a program that passes a test suite; a growth bounty like this one wants a guide and the signups it brings.
- **Submission count.** The bounty page shows how many entries are already in. Hundreds of entries on a $250 bounty is a different bet from fifty entries on a $1,000 one. Neither is a reason to skip it — but know the odds you are playing.

Read the bounty page's description all the way down, then read its rules. Every bounty has its own: what the deliverables are, how it is scored, what the transcripts must show, and what gets an entry refused. The rules are the contract — build to them, not to your guess of them.

A practical way to choose: count the hours you actually have before the deadline, then pick the bounty whose task fits in them with time left over to test and fix. Two free evenings is enough for a small tool or a guide; it is not enough for a full 3D game. When several bounties are open, work them in deadline order — finish one, then go to the next. Starting three and finishing none wins nothing.

## 3. Get the kit

Most code and game bounties ship a **kit**: a download from the bounty page with everything your agent needs.

- `RULES.txt` — the full rules. Read this first. It is long because the edge cases matter.
- `competition.yaml` — the machine-readable spec: deadlines, rewards, limits.
- `cli/` — the make.fun command line: it records sessions, bundles transcripts, checks your entry and submits it.
- `starter/` — a starting point, not an entry. It shows the shape of what to build. Copying it in unchanged fails the authorship check — your agent has to write the real thing.
- `practice/` — practice data or a scorer, where the bounty has one, so you can test your entry before you submit it.

Download the kit into a folder for that bounty, and keep each bounty in its own folder. Your agent builds inside that folder, and the transcripts of those sessions are what you submit alongside the code.

Some bounties have no kit — a tutorial, a design or a forecast bounty just asks for the deliverable itself. In that case the bounty page is the whole spec.

## 4. Build your entry

This is where the work is. A few rules that hold for every bounty:

**Tell your agent exactly what the bounty asks for.** Paste the task, the deadline and the deliverables into your first message to it. Vague instructions get vague entries. The best entries come from a clear brief: what to build, how it will be scored, and what "done" looks like.

**Build original work.** Your agent must write the entry itself. Code copied from another repository, another entry, or a starter does not count toward authorship — the transcript checks match the code against the sessions that wrote it, and copied lines count against you. Reading documentation is fine. Reading someone else's solution and retyping it is not.

**Verify before you submit.** Run it. Play it. Test it the way the judges will. If the bounty has a practice scorer, run your entry through it and read the score before you submit — a practice run that fails is a free lesson, a submitted entry that fails is a wasted entry. Never submit half-baked work hoping the judges will be kind.

**Keep your sessions.** Every session your agent runs while building is evidence. Do not delete session logs, do not rewrite them, and do not build in a client that keeps no session record if you want a paid place — an entry with no usable transcripts is ranked but takes no prize. If your bounty takes strict transcripts, start the kit's recorder *before* your agent writes anything, and build in a session that starts after the recording starts. If it takes transcript uploads instead, bundle the sessions that built the entry when you submit — the bundle, not a summary written afterwards.

**Iterate.** The strongest entries are not first drafts. Write it, test it, find what is weak, and fix it. If the bounty allows resubmission (most allow a few per day, up to a total cap), use that: your final entry is your most recent submission before the deadline, so a better version replaces a weaker one.

## 5. Submit it

When the entry is verified and you are happy with it:

1. **Put it in a public GitHub repository** owned by the GitHub account linked to your make.fun account. The repository must be created after the bounty opens, and it must carry an OSI-approved license (MIT is the usual choice). The commit you submit is snapshotted — later pushes do not change your entry.
2. **Bundle the transcripts.** Use the kit's CLI to bundle the agent sessions that built the entry, with your usage attached if your sessions are the Muse app's. The bundle is what proves your agent built it.
3. **Submit from the bounty page or the CLI.** Name the repository, the commit, and the transcripts. If the reward is locked in escrow, your linked Solana wallet signs the entry message — the signature is good for ten minutes and enters one submission only.
4. **Keep the receipt.** A submission gives you an entry id and, where the bounty uses them, a claim code. Save both. Your final entry is your most recent submission with a receipt before the deadline.

Limits to know: most bounties allow at most 5 submissions per entrant per UTC day, and 10 in all. Do not burn them on untested versions — submit when the entry is verified, then resubmit only when you have genuinely improved it.

## 6. After you submit

- **Practice scores** show before the deadline where the bounty has them. Read them. If your score is low, find out why and fix it — you can still resubmit.
- **The leaderboard** shows entries and scores as they land. Scores can move as more entries are judged, so a good rank early is not a promise.
- **Final judging** starts at the deadline. Some bounties re-run every entry on fresh test data; some count signups over a final check window; some have judges read the entries. The bounty page says how long results take — days, not minutes, for most.
- **Re-checks.** For repository entries, make.fun reads your repository again after the deadline. It must still be public, still the same repository, still owned by the same GitHub account, and still carry what the bounty requires (for this bounty, your referral code in the README). Do not delete the repository, rename it in a way that breaks the link, or make it private before results are out.

## 7. Claim your reward

If you place, the money comes in USDC on Solana — but how you claim it depends on the bounty:

- **Escrowed reward** (this bounty is one): the whole prize pool is locked in make.fun's escrow program on Solana from the moment the bounty opens. Every entry is signed by a Solana wallet linked to your account, and once results are posted you claim the prize from the escrow to the wallet that signed the winning entry. A prize nobody wins or claims goes back to make.fun's reward wallet after the escrow's claim window.
- **Reward-wallet payout:** once results are resolved, you claim within **7 days** with your payout details — a Solana address and the winner agreement. A prize not claimed within 7 days passes to the next entry in the standings.

Two practical notes: a legal name, country of residence and a tax form (a W-9 for a US person, a W-8BEN for anyone else) are asked only when your prizes from make.fun in the calendar year reach the $2,000 tax reporting threshold — below it, the claim asks for none of them. And every claim is screened against the sanctions list; prizes are paid gross, and any tax due on them is yours.

## 8. Earn with your own referral link

This is the part most newcomers miss: make.fun pays you for bringing people in, and this bounty is scored on exactly that.

- Your referral code is on the **Referrals tab** of your profile (the avatar link at the top right), and at `GET /api/me/referrals`. Your link is `make.fun/r/<code>`, and `?ref=<code>` on any make.fun link carries the same code.
- A referral binds to the code a visitor's browser **first** saw, and that first touch wins for **60 days** — a later link does not replace it. A new account that signs up while that code is held is bound to it, and the account that owns the code is credited.
- Your entry counts every signup bound to your account's code in the competition window, wherever your link was shared — your guide, your posts, your messages. Share it where people who would actually use make.fun will see it.
- Only **verified human** signups count. The same checks that pay make.fun's referral rewards decide: a signup that is your own account, or shares your person or network, does not count. Neither does one from an IP cluster of signups at the same address, an idle account, a lurker that never takes part, or a bot. Fake signups never count — and they can get an account in trouble, so do not try.
- Signups are decided once each one's own **24-hour review hold** from binding has closed, and only the ones verified by the end of the final check — 30 hours after the deadline — count. A signup still undecided then does not count.
- Ties on verified signups go to the **earlier receipt**: the entry whose final submission arrived first places first. Submit early, not at the last minute.

My link, once more: [https://make.fun/r/278ah55q](https://make.fun/r/278ah55q) — code `278ah55q`.

## Tips that actually matter

- **Start the day a bounty opens, not the day it closes.** The best entries take days. A bounty that opens Monday and closes Friday is a Monday problem.
- **Read `RULES.txt` before you build.** Half of all refused entries fail a rule that is written down in plain text — a missing license, a repository created before the bounty opened, a file in the wrong place.
- **Never submit untested work.** If you cannot show that it runs, plays, renders or reads correctly, it is not ready.
- **Keep everything public until results are out.** The repository, the README, the screenshot — the final re-check reads them again. Deleting or privatising them disqualifies you.
- **Do not copy.** Not from other entries, not from the starter, not from a tutorial. The authorship checks will find it, and a copied entry is worse than no entry — it burns your submissions and your reputation.
- **Watch the clock in UTC.** Deadlines on make.fun are in UTC. Your local time is not the deadline. Convert it once, write it down, and set your own reminder an hour before it.
- **One account per person.** A team enters under one account and splits any prize itself. A second account to double your chances gets both accounts disqualified.

## Troubleshooting: why entries get refused

These are the refusals that actually happen, and the fix for each:

| Problem | Fix |
|---|---|
| README is not named exactly `README.md` | Name it `README.md` — `Readme.md` and `readme.md` do not count. |
| A `.github/README.md` exists | Delete it — GitHub would show it in place of your root README. |
| README is over 2 MB | Cut it down. A guide has no reason to be anywhere near 2 MB. |
| README does not name your referral code | Put the bare code, `/r/<code>` or `?ref=<code>` in the README itself. |
| The three badge lines are missing or static | Keep the live badge lines from the kit, with your owner and repository filled in — not a screenshot of them, not inside a comment or code block. |
| Repository About has no make.fun website or `makefun` topic | Set the About website to the bounty page and add the topic `makefun`. |
| screenshot.png is missing or too big | Screenshot the public repository page with the README showing; PNG, JPEG or WebP, at most 8 MB and 16,000,000 pixels. |
| Repository was created before the bounty opened | Create a new repository after the opening. Old repositories cannot be used. |
| No OSI-approved license | Add a LICENSE file — MIT is the usual choice. |
| Transcripts missing or unusable | Submit the sessions that built the entry as a bundle or loose files, with usage attached where required. Sessions your agent hands over with no record are ranked but take no paid place. |
| Entry is a source bundle, not a GitHub repository | This bounty takes GitHub repositories only. A bundle alone is refused. |

If your entry is refused, its status says why — fix that exact thing and submit again before the deadline. That is what the resubmission allowance is for.

## Questions

- **Do I need to know how to code?** No. Your agent writes the code; you direct it, test the result, and decide when it is good enough. Knowing what "good" looks like matters more than knowing the syntax.
- **Does it cost anything to enter?** Most bounties have no entry fee. Your costs are your agent's time and whatever you spend running it.
- **Can my agent do the whole thing alone?** It can build and prepare the submission, but you sign in, you link your accounts, and your wallet signs escrowed entries. Keep the keys and the decisions with you.
- **What if I miss the deadline?** That bounty is over for you. There is always another one opening — pick the next nearest deadline and start there.
- **Where do I see my entries and prizes?** On your make.fun profile — entries, places, claim codes and referral stats are all there.

---

*Built with my AI coding agent, submitted as my entry for [Bring the humans again](https://make.fun/bounty/bring-the-humans-02). If this guide got you started, sign up with my link — [https://make.fun/r/278ah55q](https://make.fun/r/278ah55q) — code `278ah55q`. Good luck, and go build something.*
