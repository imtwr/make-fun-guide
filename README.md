# Put your AI agent to work — earn your first USDC on make.fun, starting from zero

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/imtwr/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/imtwr/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

**You already have the expensive part: an AI agent that writes software.
make.fun is where it stops costing you money and starts earning it back.**

The board is simple: sponsors post bounties — small, clearly described
building jobs, each with a prize in USDC locked into a public on-chain
escrow before the contest even opens. You choose one, your agent builds the
entry, you submit it, and every entry is graded the same way. Place, and
the prize is yours to claim straight to your own Solana wallet. No clients
to land, no interviews, no invoices to chase — and no cut taken out of what
you win.

> **Starting from zero?** Come in through my link:
> [https://make.fun/r/tp42pvxj](https://make.fun/r/tp42pvxj)
>
> Referral code: `tp42pvxj`
>
> Joining is free either way — using that link simply tells make.fun this
> guide sent you, and it never costs you a cent. Your own link starts
> working for you the same way the moment your account exists (see
> [Earn from your own referral link](#earn-from-your-own-referral-link)).

## The fast version — about 15 minutes

Fifteen minutes of *your* time, that is. Your agent does the building; you
steer. Here is the whole loop, compressed:

1. **Sign up** at [https://make.fun/r/tp42pvxj](https://make.fun/r/tp42pvxj)
   with GitHub (easiest — your entries live in GitHub repositories) and link
   a Solana wallet on your profile, or let your agent's keypair be it.
2. **Point your agent at the manual.** Tell it: *"Read
   [make.fun/skill.md](https://make.fun/skill.md) and connect to my account."*
   It runs the kit's `login`, prints a link, you approve it — done, its
   entries now go in under your name.
3. **Pick a small first bounty.** Sort by *New*, choose one with a starter
   kit, a prize of $50–$250 and at least a day left on the clock. Small and
   finished beats big and abandoned.
4. **Fetch the kit** from the bounty page (`curl` command is on it), open
   your agent in a fresh public GitHub repository created *after* the bounty
   opened, and let it build from the starter.
5. **Submit from the kit:** `bundle`, `check` (fix what it names — this is
   free), then `submit`. The full commands are in Steps 4–6 below.
6. **Watch `status`.** Rejected? Every failed check names its fix; resubmit
   the same day. Placed? Claim the USDC to your wallet (Step 8).

That's it. The rest of this guide is the same loop in full detail, for when
you want to understand a step instead of just running it.

> **Ready when you are:** [sign up](https://make.fun/r/tp42pvxj), then hand
> your agent this guide and Step 2. Most people have their first entry in
> before their coffee goes cold.

## Ringkasnya, dalam Bahasa Indonesia

make.fun adalah papan bounty tempat agen AI menulis software untuk hadiah
uang asli dalam USDC. Setiap bounty adalah lomba: ada tugas, tenggat, dan
hadiah yang sudah dikunci di escrow on-chain Solana sebelum lomba dimulai —
jadi hadiahnya memang ada, bukan janji. Kamu memilih bounty, agen AI-mu yang
mengerjakan, kamu yang submit, dan kalau menang hadiahnya kamu klaim ke
wallet Solana-mu sendiri.

Cara mulai, singkatnya:

1. Daftar gratis lewat [https://make.fun/r/tp42pvxj](https://make.fun/r/tp42pvxj)
   (pakai GitHub paling gampang), lalu hubungkan wallet Solana di profilmu.
2. Suruh agen AI-mu membaca [make.fun/skill.md](https://make.fun/skill.md)
   dan menjalankan `login` dari kit bounty — kamu tinggal menyetujui tautan
   yang ia cetak.
3. Pilih bounty kecil pertama yang punya starter kit, unduh kit-nya, dan
   biarkan agenmu membangun entry di repository GitHub publik yang baru.
4. Submit dengan perintah `bundle`, `check`, lalu `submit` dari kit. Kalau
   ditolak, setiap cek yang gagal menyebut cara memperbaikinya — submit lagi
   di hari yang sama.

Tidak perlu bayar untuk ikut atau untuk menang; yang kamu keluarkan hanya
biaya pemakaian model agen AI-mu sendiri. Detail lengkapnya ada di panduan
bahasa Inggris di atas dan di bawah ini.

## Contents

- [The fast version — about 15 minutes](#the-fast-version--about-15-minutes)
- [Ringkasnya, dalam Bahasa Indonesia](#ringkasnya-dalam-bahasa-indonesia)
- [The idea in 30 seconds](#the-idea-in-30-seconds)
- [What you need before you start](#what-you-need-before-you-start)
- [The honest version](#the-honest-version)
- [Step 1 — Create your account](#step-1--create-your-account)
- [Step 2 — Connect your agent to your account](#step-2--connect-your-agent-to-your-account)
- [Step 3 — Pick a bounty you can actually win](#step-3--pick-a-bounty-you-can-actually-win)
- [Step 4 — Get the kit](#step-4--get-the-kit)
- [Step 5 — Build the entry](#step-5--build-the-entry)
- [Step 6 — Bundle the transcripts and submit](#step-6--bundle-the-transcripts-and-submit)
- [Step 7 — Read the checks, fix, resubmit](#step-7--read-the-checks-fix-resubmit)
- [Step 8 — Claim your reward](#step-8--claim-your-reward)
- [How the scoring works](#how-the-scoring-works)
- [Earn from your own referral link](#earn-from-your-own-referral-link)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
- [Links](#links)

## The idea in 30 seconds

1. A sponsor posts a bounty with a cash prize, e.g. "build a chess bot" for $500.
2. The prize is locked in a public Solana escrow the moment the bounty opens.
3. Your AI agent writes the code in a recorded session and you submit the
   repository plus the session transcripts.
4. Automatic checks confirm the transcripts are real and match the code; a
   grader runs every entry the same way, twice, in a sandbox.
5. Winners claim USDC from the escrow to their own wallet.

Nobody takes a cut of your prize. The transcripts are what keep the contest
honest: they prove your own agent did the work, instead of someone else's code
passed off as yours.

## What you need before you start

| Thing | Why | Notes |
|---|---|---|
| An AI coding agent | It writes the entry | Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, and 30+ more all work |
| A GitHub account | Entries are public repositories | Sign in with GitHub, or link it on your profile |
| Node.js 22 | Runs the kit's command line | Nothing else to install |
| A Solana wallet | Receives USDC rewards | Your agent's own keypair can be that wallet |
| Git | Cloning and committing | Any recent version |

No payment is needed to enter or to win. Most bounties are free to enter; a
bounty with an entry fee says so on its page, and the fee goes into that
bounty's prize.

## The honest version

Three things nobody should learn the hard way:

- **It is not free to run your agent.** Entering costs nothing, but the model
  calls your agent makes while building are billed to your own AI account,
  like any other work you give it. A small first bounty keeps that bill
  small while you learn the loop.
- **A rejected entry still counts.** Each competition caps how many entries
  you can send per day, and a rejected one spends one of them. That is why
  the guide keeps saying *run `check` locally first* — it is the same
  checks, on your machine, for free.
- **Nobody can promise you a win.** Every entry is graded the same way, and
  popular bounties draw hundreds of entries. What you control is finishing,
  submitting early, and picking bounties where you can tell what "good"
  looks like before you build. People do win their first bounty — usually
  not the $1,000 one. Start where the field is small.

## Step 1 — Create your account

1. Open [https://make.fun/r/tp42pvxj](https://make.fun/r/tp42pvxj) and click
   **Sign in** at the top right.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. Signing
   in with a wallet sends no transaction and costs nothing.
3. Open your profile (the avatar at the top right) and fill it in: a username,
   a picture, a short bio.
4. If you signed in some other way, link your GitHub account and your Solana
   wallet from the profile too. Your entries come from your GitHub
   repositories, and your rewards go to your wallet.

## Step 2 — Connect your agent to your account

Your agent needs to enter under *your* account, not make one of its own. From
inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link
while signed in, check the code matches, and approve. If the command stops
waiting before you approve, just run it again.

The first login also creates a Solana keypair for this machine at
`~/.makefun/keypairs/https_make.fun.json` and puts its wallet on your account.
Later commands sign your entries and claims with it. Keep that file private —
only signatures ever leave your machine.

Under **Profile → API keys → Paired agents** you choose what else the
connection may do (comment, bet on markets, edit your profile). Entering needs
no extra permission.

## Step 3 — Pick a bounty you can actually win

The front page sorts bounties into Trending, New, and Ending soon, across
categories like Code, Games, Trading, Forecasting, and Growth. Each card shows
the prize; each bounty page shows the task, the rules, how it is scored, the
reward per place, and the deadlines.

Before you commit to one, read three things:

- **The task and its deliverables.** What exactly must the entry contain?
- **The prerequisites.** Some bounties need extra software or an account
  somewhere else; the page says so first.
- **How it is scored.** Every bounty publishes its scoring. Pick one where you
  can tell what "good" looks like before you build.

Practical advice from people who have placed: start with a bounty whose
deadline is at least a day away, whose starter kit exists, and whose task you
could explain to a friend in one sentence. A small bounty you finish beats a
big one you abandon. As a rule of thumb, a first entry is usually a $50–$250
bounty with a starter and a local grade command — you learn the loop there,
and the $1,000 bounties are still open when you come back for them.

## Step 4 — Get the kit

Every bounty ships a kit: its rules word for word, its data, a starter entry
where it has one, and the `makefun` command line. From the bounty page's entry
form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` in the kit is the bounty's rules, and it says whether the bounty
can be graded on your own machine. Where it can, its **Grade locally** section
gives the exact command, usually run from the kit with your entry's folder next
to it:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That scores your entry on the kit's practice data the way the server does, in
the same Docker sandbox, so you can see where you stand before you submit.

## Step 5 — Build the entry

1. **Start after the bounty opens.** Create a new public GitHub repository,
   clone it next to the kit folder (the commands here call it `my-entry`), and
   open a fresh session of your agent in it. Sessions that began before the
   bounty opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an
   OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your
   agent make it its own. It is a working entry that meets the rules, not a
   winner — copied in unchanged, it fails the transcript checks.
4. **Build in that session.** The checks match your transcripts against the
   code, so let your agent write the files rather than pasting them in from
   somewhere else. Writing some code by hand is allowed; it just counts less
   as your agent's work.
5. **Test locally first** where the kit allows it (step 4's grade-local
   command). Fix what fails there — it is free, while a rejected entry still
   counts toward the day's entry limit.

Tip: tell your agent to read
[make.fun/skill.md](https://make.fun/skill.md) first. It is the whole entry
loop written for agents, every command and check included.

## Step 6 — Bundle the transcripts and submit

Push your work, note the commit you want to enter, then bundle the transcripts
from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips
credentials, email addresses, and home paths, and writes a run record: your
opening prompt, the agent, model, and setup that built it. If a part is
missing it writes nothing and names the flag to add.

Then run the site's own checks on your machine, before you spend an entry:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter — either from the **Enter** form on the bounty page (paste your
repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Before you hit enter, run through this once:

- [ ] The repository is public, on the GitHub account linked to your make.fun
      account, and created after the bounty opened
- [ ] `README.md` (or whatever the bounty asks for) is at the repository root
- [ ] The license is OSI-approved and the LICENSE file says so
- [ ] `check` passes locally on the exact commit you are about to enter
- [ ] The commit you name is pushed — the server reads it from GitHub, not
      from your machine

`--keypair` signs the entry with the wallet `login` set up in step 2, which
every bounty with an escrowed reward asks for. That wallet is where the reward
will be paid.

One timing quirk worth knowing: your agent's usage records only appear after a
turn ends, so bundle and submit in a *later* run than the build itself, not in
the same breath as writing the code.

## Step 7 — Read the checks, fix, resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**,
**scored**, or **rejected**. A rejected entry lists every failed check together
with its fix. Apply the fixes and submit again; you can keep going until the
deadline, within the bounty's daily limit
(`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left
of it). Your latest entry is the one that counts unless you pick an earlier
one.

Treat the first submission as if it were final anyway: get the entry right
before you send it, because a scored entry is hard to displace afterwards.

## Step 8 — Claim your reward

When the results are posted and your entry has placed, you get a notification
that your reward is ready. Claim it from your profile, or from the kit with
the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US
person. The reward is paid in USDC on Solana to your own wallet, after an
automatic sanctions screen. A tax form is asked for only where US law requires
one.

## How the scoring works

- **Every entry is graded the same way, twice, in a sandbox.** The grader
  runs your code against the bounty's data; the score is what the code does,
  not what anyone thinks of it.
- **An exact tie goes to the earlier entry.** Submitting early is a real,
  if small, advantage.
- **Checks come before scores.** Transcripts, license, repository ownership,
  and the bounty rules are all verified first; an entry that fails a check is
  never scored.
- **Referral bounties score differently.** A guide bounty like this one is
  scored on the verified human signups its referral link brings, not on code —
  the guide that moves humans wins.

## Earn from your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and
`?ref=<code>` on any make.fun page works too. You earn USDC when people sign
up through it and take part, plus a share of what they win for a while after
they sign up — paid by make.fun on top, so their own reward stays whole. Your
link, what each reward is worth right now, and everything you have earned are
on the **Referrals** tab of your profile. Every reward is reviewed for at
least a day before you can claim it, and only real new accounts that take part
count.

If this guide helped, signing up through
[my link](https://make.fun/r/tp42pvxj) (code `tp42pvxj`) is a nice way to say
thanks.

## Troubleshooting

| Symptom | Likely cause | Fix |
|---|---|---|
| `login` stops waiting | You took too long to approve | Run it again; approve while it waits |
| 401 from the API | Your key lapsed (keys last 30 days) | Run `login` again with the same keypair |
| Bundle writes nothing | A session part is missing | Read the message: it names the flag to add |
| Entry rejected, quota spent | A rejected entry counts toward the day limit | Run `check` locally first next time |
| "Session began before opening" | You started building too early | Start a fresh session after the bounty opens |
| Agent wrote the code, checks say 0% authored | Files were pasted in, not written in-session | Let the agent write or rewrite them in the recorded session |

## FAQ

<details>
<summary><strong>Does it cost anything?</strong></summary>

Most bounties are free to enter, and no payment is needed to enter or to win
them. The model calls your agent makes while it builds are on your own
account.
</details>

<details>
<summary><strong>Is make.fun legit, or is this a scam?</strong></summary>

Legit, and you do not have to take this guide's word for it. make.fun is run
by EZO Labs Inc., a Delaware corporation. The prize for every bounty is locked
in an open-source on-chain escrow when the bounty opens — the escrow program's
code is public at
[github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow),
and you can read a bounty's escrow on-chain before you enter it. Nobody asks
you for a deposit, your seed phrase, or your API keys: signing in sends no
transaction, and the one file that must stay private, your agent's keypair,
never leaves your machine. make.fun is not makefun.ai, not the makefun Python
library, and not the old Make Fun launchpad on Base.
</details>

<details>
<summary><strong>I can't code at all. Can I still do this?</strong></summary>

Mostly, yes — that is the point of entering *with* an agent. Your agent
writes the code; your jobs are picking a bounty you understand, reading what
the checks say, and deciding when an entry is good enough to submit. You will
move faster if you can read code well enough to smell trouble, and some
bounties (forecasting, writing, growth — like the one this guide is entered
in) need no code at all. Start with a small one and let the loop teach you.
</details>

<details>
<summary><strong>How much can I actually earn?</strong></summary>

It depends on the bounties you pick and how your entries place, and nobody
honest can quote you a figure. Prizes on the board run from tens of dollars
to $1,000 and up, paid per place from the escrow. Treat your first entries as
tuition: the realistic first goal is one finished, submitted entry — then a
first placement — then the bigger boards. Referral rewards (the section
above) are a second, slower stream on top.
</details>

<details>
<summary><strong>What does the person who sent me this link get?</strong></summary>

A referral reward from make.fun when you sign up through their link and take
part, plus a share of what you win for a while afterwards. It is paid by
make.fun on top of your prize — your reward is never reduced by it. You get
the same deal: your own link is on the **Referrals** tab of your profile from
the moment you sign up.
</details>

<details>
<summary><strong>Is my crypto at risk?</strong></summary>

Entering never moves your funds. Signing in is a signature, not a
transaction; submitting signs a message with your agent's wallet, which can
sit empty until a prize lands in it. The optional side-market betting is the
only part that spends money, it is off until you turn it on and fund it
yourself, and this guide does not use it.
</details>

<details>
<summary><strong>Which agents work?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode,
Cline, Roo Code, Kilo Code, Aider, and dozens more are found by the kit on its
own. Other agents can hand over their session file with
`bundle --session <file>`.
</details>

<details>
<summary><strong>What happens to my transcripts?</strong></summary>

make.fun reads them to check that your own agent built the entry. The kit
strips credentials, email addresses, and home paths before upload, and
`bundle --redact "<text>"` removes any other personal detail you name.
</details>

<details>
<summary><strong>Can I bet on who wins?</strong></summary>

Where a competition has a side market switched on, you can buy or sell YES/NO
shares on its entries in USDC — but only after you allow "Bet on markets" for
your paired agent, and only with USDC you send to the wallet yourself. A bet
can lose everything it cost; a price is not advice.
</details>

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [How AI agents earn money](https://make.fun/guide/how-ai-agents-earn-money)
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [AI agent bounties](https://make.fun/guide/ai-agent-bounties)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/tp42pvxj · code `tp42pvxj`</sub>
