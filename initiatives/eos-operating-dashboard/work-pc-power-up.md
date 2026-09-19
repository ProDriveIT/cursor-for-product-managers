# Work PC power-up — EOS Phase 1

**Open this before diving into Cursor.**  
Phase 1 = Leadership **L10 board only** (Issues, Rocks, To-Dos, KPIs).  
Focus Day **1 Oct 2026** = Rob Liddiard — **no dashboard**.

---

## 0. Sit down (2 minutes) — do not open a terminal yet

Answer out loud:

1. **What is today’s one job?** (pick one)  
   - [ ] Get Bruce/Matt C′ sign-off  
   - [ ] Prep / run an L10 bake-off  
   - [ ] Provision Azure host (`az login`)  
   - [ ] Fix a named L10 board bug blocking bake-off  
   - [ ] Something else → write it in one sentence: _______________

2. **What am I explicitly not doing today?**  
   - Focus Day product / quarterly dash  
   - Client monthly reports  
   - Department Traction / AI / Matt async  
   - Dual-write Lists + GitHub  
   - “While I’m here” refactors

3. **Success for this session** (one observable): _______________

If you can’t name #1 in one line, stop. Read [`roadmap.md`](./roadmap.md) only.

---

## 1. Orient (5 minutes)

| Check | Action |
|-------|--------|
| Date vs Focus Day | Today is _____. Focus Day is **1 Oct**. Dashboard stays **closed** that day. |
| Repos | Toolkit: `cursor-for-product-managers` on `main`. Eng: `ProDrive-EOS` on `main`. |
| Decision | C′ still needs Bruce + Matt written sign-off on the 1-pager. |
| Next L10 slot | Bake-off candidates: **Mon 22 Sep**, **Mon 29 Sep**. |

Read only if stuck:

- [`roadmap.md`](./roadmap.md)  
- [`prd/1-pager-eos-operating-dashboard.md`](./prd/1-pager-eos-operating-dashboard.md)  
- Eng runbook: https://github.com/Pro-Drive-IT-Limited/ProDrive-EOS/blob/main/prodrive/deployment/Dashboard-Bakeoff-Runbook.md  

Do **not** start by browsing the whole ProDrive-EOS tree.

---

## 1b. Desktop & Cursor setup (once, then per session)

### Folder layout (clone once)

```
C:\work\ProDriveIT\cursor-for-product-managers     ← PM toolkit (roadmap, power-up, 1-pager)
C:\work\Pro-Drive-IT-Limited\ProDrive-EOS          ← eng (dashboard, Azure IaC)
```

Auth: Cursor signed in + Git for Windows + `gh auth login` (or HTTPS/SSH) as an account that can see **both** orgs. Azure CLI installed for Lane C.

### One folder = one window (default)

**Do not** open a multi-root `.code-workspace` as your main AI workspace. Rules, skills, and `AGENTS.md` are project-scoped; multi-root muddies Agent context.

| Today’s lane | Open this folder |
|--------------|------------------|
| A — Sign-off / roadmap / power-up | `cursor-for-product-managers` |
| B — Bake-off (run dashboard) | `ProDrive-EOS` |
| C — Azure provision | `ProDrive-EOS` |
| D — Eng fix | `ProDrive-EOS` |

Need both visible? **Two Cursor windows**, one folder each — not one combined workspace.

### Mode cheat sheet

| Mode | When |
|------|------|
| **Ask** | Orient, “where is X?”, read-only before touching files |
| **Plan** | Multi-file change you want to approve before Build |
| **Agent** | Implement, run `build.py` / server, guided `az` with your approval |
| **Inline Edit (Ctrl+K)** | Tiny change in the open file |
| **Tab** | Autocomplete while you type — not for IaC/bake-off workflows |

Switch with **Shift+Tab** or the mode picker. **New chat when the lane changes** (modes/chats don’t share context well across jobs).

### Per-repo instructions

| Opened folder | What the agent should pick up |
|---------------|-------------------------------|
| Toolkit | `.cursor/skills/`, `initiatives/eos-operating-dashboard/`, this power-up |
| ProDrive-EOS | root `AGENTS.md`, `prodrive/deployment/Dashboard-Bakeoff-Runbook.md` |

Toolkit skills are **not** available if only EOS is open (unless you copy them to user skills). Open the matching repo.

### Agent approvals (Windows)

Settings → Agents → Approvals: keep review on for shell. First `az login` / provision: approve yourself. Don’t let Agent run destructive Azure without you watching.

### Per-session IDE steps (after §0)

1. File → Open Folder → **lane’s repo** (table above).  
2. Wait for indexing.  
3. `git checkout main && git pull`.  
4. Open this file (toolkit) or the bake-off runbook (EOS).  
5. New chat → correct mode → paste first-message template (§3).  

---

## 2. Pick the lane (one only)

### Lane A — Sign-off (no code)

1. Open 1-pager sign-off table.  
2. Message Bruce + Matt: C′ = CEOS L10 board; Lists not the meeting board; bake-off = 2 L10s.  
3. Capture Approve/Reject + date.  
4. Stop.

### Lane B — Bake-off prep / run (primary product lane)

```bash
cd ProDrive-EOS
git checkout main && git pull
python dashboard/build.py
python apps/eos-dashboard/server.py   # http://localhost:8000/
```

In the meeting: share screen → L10 tab → stay on Rocks / Scorecard / Issues / To-Dos.  
**Do not** open SharePoint Lists as the board.  
After: note prep minutes, off-screen fetches, agenda remixes. Update checklist in initiative README.

### Lane C — Azure host (only if bake-off blocked by “no shared URL”)

Requires this machine’s `az login`.

```bash
az login
az account set --subscription "<id>"
./prodrive/deploy/azure/provision.sh <rg> uksouth
./prodrive/deploy/azure/deploy-app.sh <rg> <webAppName>
```

Then Easy Auth → tenant `fe099a0d-5df8-41bd-a4cf-9047d90735bd` → Leadership only.  
If auth takes >30 minutes, abandon and use localhost share-screen for bake-off.

### Lane D — Eng fix (only with a named bake-off blocker)

1. Write the blocker in one sentence.  
2. Branch: `cursor/<short-blocker>-d8ca` off `main`.  
3. Smallest fix. Draft PR. No drive-by cleanup.

---

## 3. Cursor IDE habits (stay out of the rabbit hole)

| Do | Don’t |
|----|--------|
| Open the **lane’s repo** only | Multi-root workspace “so everything is there” |
| Ask → Plan → Agent as needed | Agent-everything before you can name the job |
| One chat = one lane | “Also stand up Focus Day / reports / API” |
| Paste this checklist + today’s one job into the first message | Paste the whole company history |
| Point at `roadmap.md` + runbook | Ask the agent to “improve the EOS platform” |
| Timebox: 25–45 min, then re-check §0 | Open Azure portal “just to look” mid-bake-off |
| End session with: done / next / parked | Leave half-finished IaC as the mental state |

**First message template:**

> Phase 1 L10 only. Focus Day 1 Oct = no dashboard.  
> Today’s one job: **[lane + sentence]**.  
> Do not touch Focus Day product, client reports, or Lists-as-board.  
> Opened folder: **[toolkit | ProDrive-EOS]**.  
> Relevant: `initiatives/eos-operating-dashboard/roadmap.md` (toolkit) or `prodrive/deployment/Dashboard-Bakeoff-Runbook.md` (EOS).

---

## 4. Power-down (3 minutes)

- [ ] Checklist item updated (sign-off / bake-off # / Azure)  
- [ ] Commit/PR only if eng changed  
- [ ] Tomorrow’s one job written: _______________  
- [ ] Anything that smelled like scope creep → parked note, not a branch  

---

## Kill switches (stand up and walk away)

- Building anything for **1 Oct Focus Day** → stop.  
- Editing SharePoint Lists “so the meeting works” → stop.  
- Starting client monthly reports → stop (separate initiative).  
- Azure Easy Auth rabbit hole past 30 min with no URL for Leadership → fall back to localhost.  
- Agent proposing FastAPI / dual-write / quarterly dash → reject; Phase 1 is L10 board only.
