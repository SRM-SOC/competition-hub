# Contributing to SRM-SOC

Welcome to **SRM Summer of Code**! This guide covers everything you need to go from zero to your first merged PR. Read it fully before raising your first PR — it will save you time.

---

## Table of Contents

- [Before You Start](#before-you-start)
- [Registration](#registration)
- [Finding & Claiming Issues](#finding--claiming-issues)
- [Making Your Contribution](#making-your-contribution)
- [PR Format Rules](#pr-format-rules)
- [Issue Types & Points](#issue-types--points)
- [Claim Rules](#claim-rules)
- [Review Process](#review-process)
- [Getting Help](#getting-help)

---

## Before You Start

Make sure you have:
- [ ] A GitHub account
- [ ] Git installed on your machine
- [ ] Joined our [Discord server](https://discord.gg/YOUR_INVITE)
- [ ] Basic knowledge of Git (fork, branch, commit, PR)

---

## Registration

Registration is **mandatory** before claiming any issue.

1. Join the [Discord server](https://discord.gg/YOUR_INVITE)
2. Go to the `#register` channel
3. Run the command:
   ```
   /register github:your_github_username name:Your Full Name year:2nd
   ```
4. The bot will confirm and assign you the `@Participant` role
5. You are now registered — your points will be tracked automatically

> ⚠️ You cannot claim issues or earn points without registering first.

---

## Finding & Claiming Issues

### Where to find issues

- Browse the `#issues-easy`, `#issues-medium`, `#issues-hard` channels on Discord
- Go directly to any project repo on GitHub and filter by labels
- Check the [Issues board](https://YOUR_WEBSITE_URL/issues) on the leaderboard website

### How to claim an issue

Run this command in any Discord channel:

```
/claim issue:42 repo:college-utils
```

The bot will:
- Check the issue is still available
- Check you have fewer than 2 active claims
- Assign you on GitHub and start the claim timer

> You must claim an issue **before** raising a PR. PRs from unassigned contributors will not be merged.

### Claim limits

- Maximum **2 active claims** at a time
- `bug-fix`, `documentation`, `design` — **3 day** claim window
- `feature`, `enhancement` — **5 day** claim window
- If you don't raise a PR within the window, the issue is auto-unassigned

To release a claim early:
```
/unclaim issue:42 repo:college-utils
```

---

## Making Your Contribution

### Step 1 — Fork the repo

Go to the project repo on GitHub and click **Fork**.

### Step 2 — Clone your fork

```bash
git clone https://github.com/YOUR_USERNAME/REPO_NAME
cd REPO_NAME
```

### Step 3 — Create a branch

Branch names **must** follow this format:

| Issue type | Branch format | Example |
|---|---|---|
| Bug fix | `fix/issue-{number}` | `fix/issue-42` |
| Feature | `feat/issue-{number}` | `feat/issue-67` |
| Documentation | `docs/issue-{number}` | `docs/issue-15` |
| Design | `design/issue-{number}` | `design/issue-33` |
| Enhancement | `enhance/issue-{number}` | `enhance/issue-28` |

```bash
git checkout -b fix/issue-42
```

### Step 4 — Make your changes

- Keep changes focused — only fix what the issue describes
- Test your changes locally before pushing
- Do not modify files unrelated to your issue

### Step 5 — Commit your changes

```bash
git add .
git commit -m "fix: #42 short description of what you fixed"
```

### Step 6 — Push and open a PR

```bash
git push origin fix/issue-42
```

Then go to your fork on GitHub and click **Compare & pull request**.

---

## PR Format Rules

These are enforced automatically by our bot. PRs that fail these checks will not be reviewed.

### PR Title

Must follow this exact format:

```
type: #issue-number short description
```

Valid types: `fix`, `feat`, `docs`, `design`, `enhance`, `chore`

✅ Good: `fix: #42 navbar not rendering on mobile`
✅ Good: `feat: #67 add CGPA calculator export button`
❌ Bad: `fixed navbar`
❌ Bad: `PR for issue 42`

### PR Description

Fill in all sections of the PR template:

```markdown
## Linked Issue
Closes #42

## What did you change?
Brief description of your changes.

## Screenshots (if UI change)
Add before/after screenshots here.

## Checklist
- [x] My branch is named correctly (fix/issue-42)
- [x] PR title follows the correct format
- [x] I was assigned to this issue before raising this PR
- [x] I tested my changes locally
- [x] I have not copied code from another participant's PR
```

> ⚠️ `Closes #issue-number` in the description is mandatory. The bot checks for this.

---

## Issue Types & Points

| Label | Points | Open to | Window |
|---|---|---|---|
| `onboarding` | 5 | Everyone, one-time | No expiry |
| `documentation` | 10 | Everyone | 3 days |
| `first-timers-only` | 10 | 0 merged PRs only | 3 days |
| `design` | 15 | Everyone | 3 days |
| `bug-fix` | 20 | Everyone | 3 days |
| `enhancement` | 25 | Everyone | 5 days |
| `feature` | 40 | Everyone | 5 days |

### Issue access types

- **`open`** — Multiple people can submit PRs, best one gets merged and earns points
- **`first-come-first-served`** — Only the person who claims it can raise a PR (default)
- **`first-timers-only`** — Only claimable if you have 0 merged PRs in this competition

---

## Review Process

1. You raise a PR → bot automatically checks title, format, and assignment
2. If checks pass → a maintainer reviews within **48 hours**
3. Maintainer may request changes — respond to comments and push updates
4. Once approved → PR is merged → points are **automatically added** to your account
5. Bot posts in `#points-log` and `#pr-merged` on Discord

### What makes a good PR

- Solves exactly what the issue describes — no more, no less
- Clean, readable code with meaningful variable names
- No commented-out code or debug logs left in
- Works correctly and has been tested

### Reasons a PR gets rejected

- Does not solve the issue
- Copied from another participant
- Raises a PR without being assigned
- Breaks existing functionality
- Fails bot format checks

---

## Plagiarism Policy

Submitting copied code — from another participant, from Stack Overflow without adaptation, or from AI without understanding — is grounds for **immediate disqualification** from the competition. All submissions are checked.

---

## Getting Help

- Stuck on an issue? Ask in `#help-and-questions` on Discord
- Want a PR review from peers? Post in `#pr-reviews`
- Bot not working? Ping `@Maintainer` in Discord
- General questions? Check `#faq` first

---

## Your First PR — The Onboarding Issue

Not sure where to start? Your very first task is the **onboarding issue**:

1. Find it here: [Onboarding Issue](https://github.com/YOUR_ORG/competition-hub/issues/1)
2. Add your row to [CONTRIBUTORS.md](./CONTRIBUTORS.md)
3. Raise a PR to `competition-hub` repo
4. Earn your first **5 points** 🎉

This walks you through the full contribution loop in a zero-pressure way.

---

*Happy contributing! If something in this guide is unclear, open an issue on this repo and we'll improve it.*